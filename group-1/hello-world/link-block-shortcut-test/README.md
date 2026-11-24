---
noRobotsIndex: true
---

# Link block shortcut test

Test for the Apryse report: a link block references a sidebar shortcut rather than its final destination. Compare this page in the editor and on the published site.

## Direct page links — controls

{% content-ref url="appian-destination.md" %}
[appian-destination.md](appian-destination.md)
{% endcontent-ref %}

{% content-ref url="salesforce-destination.md" %}
[salesforce-destination.md](salesforce-destination.md)
{% endcontent-ref %}

## Sidebar shortcut links — reproduction

These blocks reference the existing Nostaligua and Siberia sidebar shortcuts in this space. Expected: their titles and destination URLs work just like the direct links below. Reported failure: the blocks show “space” and link to the GitBook app.

{% content-ref url="https://production-playground.gitbook.io/colossal/nostalgia-of-banal-items-through-papier-mache" %}
[Nostaligua](https://production-playground.gitbook.io/colossal/nostalgia-of-banal-items-through-papier-mache)
{% endcontent-ref %}

{% content-ref url="https://production-playground.gitbook.io/colossal/group-1/the-barber-of-siberia" %}
[Siberia](https://production-playground.gitbook.io/colossal/group-1/the-barber-of-siberia)
{% endcontent-ref %}

## Direct destination URLs — comparison

{% content-ref url="https://production-playground.gitbook.io/colossal/nostalgia-of-banal-items-through-papier-mache" %}
[https://production-playground.gitbook.io/colossal/nostalgia-of-banal-items-through-papier-mache](https://production-playground.gitbook.io/colossal/nostalgia-of-banal-items-through-papier-mache)
{% endcontent-ref %}

{% content-ref url="https://production-playground.gitbook.io/colossal/group-1/the-barber-of-siberia" %}
[https://production-playground.gitbook.io/colossal/group-1/the-barber-of-siberia](https://production-playground.gitbook.io/colossal/group-1/the-barber-of-siberia)
{% endcontent-ref %}
