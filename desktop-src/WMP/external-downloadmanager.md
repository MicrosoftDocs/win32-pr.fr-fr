---
title: External. DownloadManager
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La propriété DownloadManager récupère l’objet DownloadManager.
ms.assetid: 9fec7175-611e-4e7e-8978-132e6f86329a
keywords:
- External. DownloadManager Lecteur Windows Media
topic_type:
- apiref
api_name:
- External.DownloadManager
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55e6371f5c8d1e5dfcb17762340a82e8d921c17
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192399"
---
# <a name="externaldownloadmanager"></a>External. DownloadManager

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La propriété **downloadmanager** récupère l’objet **downloadmanager** .

``` syntax
window.external.DownloadManager
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un objet **downloadmanager** en lecture seule.

## <a name="remarks"></a>Notes

dans Lecteur Windows Media 10 ou version ultérieure, la propriété et l’objet **DownloadManager** sont accessibles uniquement à partir des volets de tâches du service de magasin en ligne. Vous ne pouvez pas utiliser **downloadmanager** à partir d’autres fonctionnalités où l’objet **externe** est disponible, par exemple HTMLView, le mode Info Center et les informations sur l’album.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 2 en ligne**](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





