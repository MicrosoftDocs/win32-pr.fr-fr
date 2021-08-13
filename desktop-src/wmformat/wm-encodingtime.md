---
title: WM/EncodingTime
description: L’attribut WM/EncodingTime contient un horodatage de l’heure à laquelle le contenu a été encodé.
ms.assetid: 63da9392-264d-40bb-99fd-56db93801941
keywords:
- Format Windows Media WM/EncodingTime
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20c76de789bd6ca88a9bbc2f3bb68381b3816524a07cbf97dc1a35b2526179a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431837"
---
# <a name="wmencodingtime"></a>WM/EncodingTime

L’attribut **WM/EncodingTime** contient un horodatage de l’heure à laquelle le contenu a été encodé.

## <a name="global-constant"></a>Constante globale

\_wszWMEncodingTime g

## <a name="data-type"></a>Type de données

**fileTime** (**\_ type WMT \_ QWord**)

## <a name="remarks"></a>Remarques

Cet attribut utilise une valeur FILETIME, qui est une valeur 64 bits représentant le nombre d’unités de temps de 100 nanosecondes écoulées depuis le 1er janvier 1601. pour plus d’informations sur FILETIME, consultez la section Windows System Information du kit de développement logiciel (SDK) de plateforme.

Il ne s’agit pas d’un attribut codé. Vous devez la définir manuellement si vous souhaitez l’inclure dans vos fichiers.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




