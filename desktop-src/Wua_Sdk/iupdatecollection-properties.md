---
description: L’interface IUpdateCollection définit les propriétés suivantes.
ms.assetid: 38420d5e-4d36-4ed7-be06-e1df903929a7
title: Propriétés IUpdateCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599e7ba6efd20810ad61a8f59f5cfec67ce82b9e95f42df5250360238c43d044
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859759"
---
# <a name="iupdatecollection-properties"></a>Propriétés IUpdateCollection

L’interface [**IUpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection) définit les propriétés suivantes.



| Propriété                                        | Description                                                                                                              |
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get__newenum) | Obtient une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) qui peut être utilisée pour énumérer la collection. |
| [**Count**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_count)        | Obtient le nombre d’éléments de la collection.                                                                           |
| [**Élément**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_item)          | Obtient ou définit une interface [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) dans une collection.                                                    |
| [**Seulement**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_readonly)  | Obtient une valeur booléenne qui indique si la collection de mises à jour est en lecture seule.                                          |



 

 

 
