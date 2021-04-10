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
ms.openlocfilehash: 9d27119a9b54e3de22fe620f556c672bd4fe1a17
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030425"
---
# <a name="wmencodingtime"></a>WM/EncodingTime

L’attribut **WM/EncodingTime** contient un horodatage de l’heure à laquelle le contenu a été encodé.

## <a name="global-constant"></a>Constante globale

\_wszWMEncodingTime g

## <a name="data-type"></a>Type de données

**fileTime** (**\_ type WMT \_ QWord**)

## <a name="remarks"></a>Notes

Cet attribut utilise une valeur FILETIME, qui est une valeur 64 bits représentant le nombre d’unités de temps de 100 nanosecondes écoulées depuis le 1er janvier 1601. Pour plus d’informations sur FILETIME, consultez la section informations système Windows du kit de développement logiciel (SDK) de plateforme.

Il ne s’agit pas d’un attribut codé. Vous devez la définir manuellement si vous souhaitez l’inclure dans vos fichiers.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




