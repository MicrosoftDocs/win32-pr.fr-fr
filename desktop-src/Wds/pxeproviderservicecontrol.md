---
title: PxeProviderServiceControl fonction de rappel
description: Appelée lorsqu’un code de contrôle de service est reçu par le service WDS.
ms.assetid: 180ddcda-d111-4c81-9177-db99cbf1449f
keywords:
- Fonction de rappel PxeProviderServiceControl des services de déploiement Windows
topic_type:
- apiref
api_name:
- PxeProviderServiceControl
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c8a2c71b7b386254622758efa5f3dc5269a131d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510321"
---
# <a name="pxeproviderservicecontrol-callback-function"></a>PxeProviderServiceControl fonction de rappel

Appelée lorsqu’un code de contrôle de service est reçu par le service WDS. Cette fonction de rappel est inscrite en appelant la fonction [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) avec le paramètre *CallbackType* défini sur le **contrôle du \_ \_ service \_ de rappel PXE**.

## <a name="syntax"></a>Syntaxe


```C++
DWORD PXEAPI PxeProviderServiceControl(
  _In_ PVOID pContext,
       DWORD dwControl
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pContext* \[ dans\]
</dt> <dd>

Valeur de contexte passée à la fonction [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .

</dd> <dt>

*dwControl* 
</dt> <dd>

Code de contrôle. Pour obtenir la liste des valeurs possibles, consultez le paramètre *dwControl* de la fonction [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’arrêt du fournisseur réussit, le rappel doit retourner la **\_ réussite** de l’erreur. En cas d’échec, un code d’erreur approprié doit être retourné.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008, Windows Server 2003 avec les \[ applications de bureau SP2 uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions du serveur des services de déploiement Windows](windows-deployment-services-server-functions.md)
</dt> <dt>

[**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

