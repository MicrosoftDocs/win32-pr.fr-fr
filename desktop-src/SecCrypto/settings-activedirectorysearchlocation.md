---
description: Définit ou récupère le Active Directory emplacement de recherche.
ms.assetid: 43320799-1c01-4e09-bed9-f3576baadcce
title: Propriété Settings. ActiveDirectorySearchLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.ActiveDirectorySearchLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d218b3d589b76980d468395a39452613aa57ada5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526738"
---
# <a name="settingsactivedirectorysearchlocation-property"></a>Propriété Settings. ActiveDirectorySearchLocation

\[La propriété **ActiveDirectorySearchLocation** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.\]

La propriété **ActiveDirectorySearchLocation** définit ou récupère le Active Directory emplacement de recherche.

## <a name="syntax"></a>Syntaxe


```VB
Settings.ActiveDirectorySearchLocation As CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
```



## <a name="property-value"></a>Valeur de la propriété

Valeur de l’énumération de l' [**\_ emplacement de \_ \_ recherche \_ Active Directory CAPICOM**](capicom-active-directory-search-location.md) qui spécifie l’emplacement de recherche. La valeur par défaut est la \_ recherche CAPICOM \_ . Le tableau suivant répertorie les valeurs possibles.



| Value                                                                                                                                                                                                           | Signification                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="CAPICOM_SEARCH_ANY"></span><span id="capicom_search_any"></span><dl> <dt>**Rechercher dans CAPICOM \_ \_**</dt> </dl>                                   | Recherchez tous les emplacements disponibles.<br/> |
| <span id="CAPICOM_SEARCH_DEFAULT_DOMAIN"></span><span id="capicom_search_default_domain"></span><dl> <dt>**\_ \_ domaine par défaut de recherche \_ CAPICOM**</dt> </dl> | Recherche uniquement dans le domaine par défaut.<br/> |
| <span id="CAPICOM_SEARCH_GLOBAL_CATALOG"></span><span id="capicom_search_global_catalog"></span><dl> <dt>**\_catalogue global de recherche \_ CAPICOM \_**</dt> </dl> | Recherche uniquement dans le catalogue global.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Paramètres**](settings.md)
</dt> </dl>

 

 




