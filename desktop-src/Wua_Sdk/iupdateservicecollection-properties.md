---
description: L’interface IUpdateServiceCollection définit les propriétés suivantes.
ms.assetid: 340a63ee-8e31-467d-88d2-f320ccc0f054
title: Propriétés IUpdateServiceCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a4292a128587d961447c29acf22aa7badc9c62e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516890"
---
# <a name="iupdateservicecollection-properties"></a>Propriétés IUpdateServiceCollection

L’interface [**IUpdateServiceCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicecollection) définit les propriétés suivantes.



| Propriété                                               | Description                                                                                                          |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicecollection-get__newenum) | Obtient une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) utilisée pour énumérer la collection. |
| [**Saut**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicecollection-get_count)        | Obtient le nombre d’éléments de la collection.                                                                       |
| [**Élément**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicecollection-get_item)          | Obtient et définit une interface [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) dans la collection.                               |



 

 

 
