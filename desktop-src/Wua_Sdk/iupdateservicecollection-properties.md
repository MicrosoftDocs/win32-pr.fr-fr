---
description: L’interface IUpdateServiceCollection définit les propriétés suivantes.
ms.assetid: 340a63ee-8e31-467d-88d2-f320ccc0f054
title: Propriétés IUpdateServiceCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d63a99d15f95c086bb8c1b062e76015f00d8214f64e5b4f73ed2832f1f5fab99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118815002"
---
# <a name="iupdateservicecollection-properties"></a>Propriétés IUpdateServiceCollection

L’interface [**IUpdateServiceCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicecollection) définit les propriétés suivantes.



| Propriété                                               | Description                                                                                                          |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicecollection-get__newenum) | Obtient une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) utilisée pour énumérer la collection. |
| [**Count**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicecollection-get_count)        | Obtient le nombre d’éléments de la collection.                                                                       |
| [**Élément**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicecollection-get_item)          | Obtient et définit une interface [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) dans la collection.                               |



 

 

 
