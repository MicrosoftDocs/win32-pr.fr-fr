---
description: L’interface IUpdateCollection définit les propriétés suivantes.
ms.assetid: 38420d5e-4d36-4ed7-be06-e1df903929a7
title: Propriétés IUpdateCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aae347885deccb52ac44513bd1138aa18995c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514032"
---
# <a name="iupdatecollection-properties"></a>Propriétés IUpdateCollection

L’interface [**IUpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection) définit les propriétés suivantes.



| Propriété                                        | Description                                                                                                              |
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get__newenum) | Obtient une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) qui peut être utilisée pour énumérer la collection. |
| [**Saut**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_count)        | Obtient le nombre d’éléments de la collection.                                                                           |
| [**Élément**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_item)          | Obtient ou définit une interface [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) dans une collection.                                                    |
| [**Seulement**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_readonly)  | Obtient une valeur booléenne qui indique si la collection de mises à jour est en lecture seule.                                          |



 

 

 
