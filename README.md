  echo "## Séries populaires sur BDplus.cc"
  echo
  echo "- [Accueil](https://bdplus.cc/)"
  echo "- [Toutes les séries](https://bdplus.cc/serie.html)"
  find /var/www/bdplus/serie_static -type f -name '*.html' \
    -printf '%T@ %p\n' | sort -nr | head -n 12 | awk '{print $2}' \
    | sed 's#^/var/www/bdplus#https://bdplus.cc#' \
    | awk -F'/' '{u=$0; s=$NF; sub(/\.html$/,"",s); gsub(/-/," ",s); printf "- [%s](%s)\n", s, u }'
} | tee /tmp/BDplus-links.md
## Séries populaires sur BDplus.cc

- [Accueil](https://bdplus.cc/)
- [Toutes les séries](https://bdplus.cc/serie.html)
- [index](https://bdplus.cc/serie_static/index.html)
- [zombillenium](https://bdplus.cc/serie_static/zombillenium.html)
- [xiii mystery](https://bdplus.cc/serie_static/xiii-mystery.html)
- [xiii](https://bdplus.cc/serie_static/xiii.html)
- [x isle](https://bdplus.cc/serie_static/x-isle.html)
- [wunderwaffen](https://bdplus.cc/serie_static/wunderwaffen.html)
- [world war x](https://bdplus.cc/serie_static/world-war-x.html)
- [wollodrin](https://bdplus.cc/serie_static/wollodrin.html)
- [wild west gloris lamontagne](https://bdplus.cc/serie_static/wild-west-gloris-lamontagne.html)
- [west fantasy](https://bdplus.cc/serie_static/west-fantasy.html)
- [west](https://bdplus.cc/serie_static/west.html)
- [waterloo](https://bdplus.cc/serie_static/waterloo.html)
