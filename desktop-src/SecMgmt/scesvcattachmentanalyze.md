---
description: La fonction SceSvcAttachmentAnalyze est appelée par le moteur de configuration de sécurité lors de l’analyse du système.
ms.assetid: 8e8a39b9-c4e2-446e-8e0c-eb2113234c1a
title: SceSvcAttachmentAnalyze fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentAnalyze
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 296d755a0b082b46122432936d30614019b8b9a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228929"
---
# <a name="scesvcattachmentanalyze-callback-function"></a>SceSvcAttachmentAnalyze fonction de rappel

La fonction **SceSvcAttachmentAnalyze** est appelée par le moteur de configuration de sécurité lors de l’analyse du système.

## <a name="syntax"></a>Syntaxe


```C++
SCESTATUS WINAPI SceSvcAttachmentAnalyze(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSceCbInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure d' [**\_ \_ informations de rappel SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) qui contient un handle de base de données opaque et des pointeurs de fonction de rappel pour interroger, définir et libérer des informations.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si cette fonction réussit, elle retourne SCESTATUS \_ Success. Sinon, elle retourne un code d’erreur. Pour plus d’informations sur les codes d’erreur de configuration de la sécurité, consultez [Attachment Return values](management-return-values.md).

## <a name="remarks"></a>Notes

La fonction **SceSvcAttachmentAnalyze** doit effectuer les opérations suivantes :

-   Interroger directement les informations de configuration à partir du service.
-   Appelez la fonction de rappel vers laquelle pointe le membre **pfQueryInfo** de la structure d' [**\_ \_ informations de rappel SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) pour récupérer les informations de la base de données de sécurité.
-   Calcule les différences entre les informations en fonction du type et de la syntaxe.
-   Appelez la fonction de rappel vers laquelle pointe le membre **pfSetInfo** de la structure d' [**\_ \_ informations de rappel SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) pour mettre à jour la base de données de sécurité avec les informations de service récupérées différentes.

Pour plus d’informations, consultez [implémentation de SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Implémentation de SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md)
</dt> <dt>

[**\_informations de rappel SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)
</dt> </dl>

 

 




