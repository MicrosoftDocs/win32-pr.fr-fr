---
title: Annexe C IAccessible DISPID
description: Un DISPID permet à l’implémentation de IDispatch de rechercher les différentes méthodes et propriétés d’une interface double.
ms.assetid: 3d19b37a-1ce4-4f34-96b3-ff39b320e8db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d510fac39209cdb268a7676b49bbb6424cae1b09
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010713"
---
# <a name="appendix-c-iaccessible-dispids"></a>Annexe C : DISPID de IAccessible

Un DISPID permet à l’implémentation de [**IDispatch**](idispatch-interface.md) de rechercher les différentes méthodes et propriétés d’une interface double.


```C++
// PROPERTIES: Hierarchical 
#define DISPID_ACC_PARENT                   (-5000)
#define DISPID_ACC_CHILDCOUNT               (-5001)
#define DISPID_ACC_CHILD                    (-5002)
                                             
// PROPERTIES: Descriptive 
#define DISPID_ACC_NAME                     (-5003)
#define DISPID_ACC_VALUE                    (-5004)
#define DISPID_ACC_DESCRIPTION              (-5005)
#define DISPID_ACC_ROLE                     (-5006)
#define DISPID_ACC_STATE                    (-5007)
#define DISPID_ACC_HELP                     (-5008)
#define DISPID_ACC_HELPTOPIC                (-5009)
#define DISPID_ACC_KEYBOARDSHORTCUT         (-5010)
#define DISPID_ACC_FOCUS                    (-5011)
#define DISPID_ACC_SELECTION                (-5012)
#define DISPID_ACC_DEFAULTACTION            (-5013)

// METHODS 
#define DISPID_ACC_SELECT                   (-5014)
#define DISPID_ACC_LOCATION                 (-5015)
#define DISPID_ACC_NAVIGATE                 (-5016)
#define DISPID_ACC_HITTEST                  (-5017)
#define DISPID_ACC_DODEFAULTACTION          (-5018)
```



 

 




