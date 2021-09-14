---
description: La fonction SceSvcAttachmentConfig est appelée par le moteur de configuration de sécurité lorsque le système est configuré.
ms.assetid: ad20649a-2391-421b-a08c-a4ea6a882abc
title: SceSvcAttachmentConfig fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentConfig
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: c78caa3b8e08ade9c674a11d113a8b91b8f5fad1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228918"
---
# <a name="scesvcattachmentconfig-callback-function"></a>SceSvcAttachmentConfig fonction de rappel

La fonction **SceSvcAttachmentConfig** est appelée par le moteur de configuration de sécurité lorsque le système est configuré.

## <a name="syntax"></a>Syntaxe


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSceCbInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure d' [**\_ \_ informations de rappel SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) qui contient le handle de base de données et les fonctions de rappel pour interroger, définir et libérer des informations.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si cette fonction réussit, elle retourne SCESTATUS \_ Success. Sinon, elle retourne un code d’erreur. Pour plus d’informations sur les codes d’erreur de configuration de la sécurité, consultez [Attachment Return values](management-return-values.md).

## <a name="remarks"></a>Notes

Lors de l’implémentation de cette fonction, utilisez la fonction de rappel vers laquelle pointe le membre **pfQueryInfo** de la structure d’informations de [**\_ rappel \_ SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) pour récupérer les informations de configuration. Configurez ensuite le service à l’aide des informations retournées.

Cette fonction doit effectuer les opérations suivantes :

-   Interroger les informations de configuration à partir de l’outil de configuration de la sécurité défini à l’aide de la fonction de rappel désignée par le membre **pfQueryInfo** de la structure SCESVC (pSceCbInfo->pfQueryInfo). [**\_ \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
-   Configurez le service à l’aide des informations de configuration.

Pour plus d’informations, consultez [implémentation de SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md)

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_informations de rappel SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md)
</dt> </dl>

 

 




