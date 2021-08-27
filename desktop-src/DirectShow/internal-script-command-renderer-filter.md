---
description: Filtre de convertisseur de commande de script interne
ms.assetid: 264cc7c3-987c-4832-85a2-087278a4d024
title: Filtre de convertisseur de commande de script interne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b70fbcd7dc6347ec93a19558ef2306dffd5fb64
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982212"
---
# <a name="internal-script-command-renderer-filter"></a>Filtre de convertisseur de commande de script interne

Reçoit des commandes de script et les distribue à l’application.

Ce filtre accepte les commandes de script dans l’un des deux formats suivants :

-   Texte du MEDIATYPE \_ : chaque exemple de média contient une chaîne de texte ANSI.
-   MEDIATYPE \_ commande : chaque exemple de média contient deux chaînes Unicode se terminant par un caractère null, concaténées ensemble. La première chaîne décrit le type de commande et la deuxième chaîne est la commande de script.

    Lorsque le filtre reçoit un exemple, il envoie une notification d’événement d' [**\_ \_ événement OLE EC**](ec-ole-event.md) . Le premier paramètre d’événement est un **BSTR** avec le type de commande, ou `Text` si le format est du texte de MediaType \_ . Le deuxième paramètre d’événement est un **BSTR** avec la commande de script. L’application peut récupérer l’événement et répondre à la commande de script.

Pour obtenir un exemple d’utilisation de ce filtre, consultez l’article sur l' [analyseur sami (CC)](sami--cc--parser-filter.md).




| Étiquette | Valeur |
|--------|-------|
| Interfaces de filtre | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a> | 
| Types de média de broche d’entrée | <ul><li>MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</li><li>MEDIATYPE_Text, MEDIASUBTYPE_NULL</li></ul> | 
| Interfaces pin d’entrée | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Types de média de broche de sortie | Non applicable | 
| Interfaces de broche de sortie | Non applicable | 
| CLSID du filtre | {48025243-2D39-11CE-875D-00608CB78066} | 
| CLSID de page de propriétés | Aucune page de propriétés | 
| Exécutable | Quartz.dll | 
| <a href="merit.md">Mérite</a> | MERIT_PREFERRED + 1 | 
| <a href="filter-categories.md">Catégorie de filtre</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 



