---
description: Inversez le service dans l’état arrêté.
ms.assetid: d7469643-bccc-4f55-b2fc-d2bc2e392d84
title: Méthode StopService de la classe CIM_Service (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9b36cab1054e99ac306fb1b21fe9f08e0820974a0883e90655a180b07035b7f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647582"
---
# <a name="stopservice-method-of-the-cim_service-class-hyper-v-management"></a>Méthode StopService de la classe CIM_Service (gestion Hyper-V)

Inversez le service dans l’état arrêté.

> [!Note]
>
> La sémantique de cette méthode se chevauche avec la méthode **RequestStateChange** héritée de [**la \_ EnabledLogicalElement CIM**](cim-enabledlogicalelement.md). Cette méthode est conservée, car elle a été largement implémentée et sa sémantique « Stop » simple est pratique à utiliser.

 

## <a name="syntax"></a>Syntaxe


```mof
uint32 StopService();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite ; Sinon, retourne une erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Service CIM**](cim-service.md)
</dt> </dl>

 

 




