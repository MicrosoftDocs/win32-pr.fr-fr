---
description: Filtre de convertisseur de commande de script interne
ms.assetid: 264cc7c3-987c-4832-85a2-087278a4d024
title: Filtre de convertisseur de commande de script interne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b241643d991e9348015dc51ea5b2f1c4875f079d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521596"
---
# <a name="internal-script-command-renderer-filter"></a>Filtre de convertisseur de commande de script interne

Reçoit des commandes de script et les distribue à l’application.

Ce filtre accepte les commandes de script dans l’un des deux formats suivants :

-   Texte du MEDIATYPE \_ : chaque exemple de média contient une chaîne de texte ANSI.
-   MEDIATYPE \_ commande : chaque exemple de média contient deux chaînes Unicode se terminant par un caractère null, concaténées ensemble. La première chaîne décrit le type de commande et la deuxième chaîne est la commande de script.

    Lorsque le filtre reçoit un exemple, il envoie une notification d’événement d' [**\_ \_ événement OLE EC**](ec-ole-event.md) . Le premier paramètre d’événement est un **BSTR** avec le type de commande, ou `Text` si le format est du texte de MediaType \_ . Le deuxième paramètre d’événement est un **BSTR** avec la commande de script. L’application peut récupérer l’événement et répondre à la commande de script.

Pour obtenir un exemple d’utilisation de ce filtre, consultez l’article sur l' [analyseur sami (CC)](sami--cc--parser-filter.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtre</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></td>
</tr>
<tr class="even">
<td>Types de média de broche d’entrée</td>
<td><ul>
<li>MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</li>
<li>MEDIATYPE_Text, MEDIASUBTYPE_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces pin d’entrée</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Types de média de broche de sortie</td>
<td>Non applicable</td>
</tr>
<tr class="odd">
<td>Interfaces de broche de sortie</td>
<td>Non applicable</td>
</tr>
<tr class="even">
<td>CLSID du filtre</td>
<td>{48025243-2D39-11CE-875D-00608CB78066}</td>
</tr>
<tr class="odd">
<td>CLSID de page de propriétés</td>
<td>Aucune page de propriétés</td>
</tr>
<tr class="even">
<td>Exécutable</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Mérite</a></td>
<td>MERIT_PREFERRED + 1</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Catégorie de filtre</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 



