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
ms.openlocfilehash: 9bb84cc6a8492c729926b644a246b8ee8a03e1de4c2eae6e3de1fd88c5ba339f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004917"
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

## <a name="return-value"></a>Valeur retournée

Si cette fonction réussit, elle retourne SCESTATUS \_ Success. Sinon, elle retourne un code d’erreur. Pour plus d’informations sur les codes d’erreur de configuration de la sécurité, consultez [Attachment Return values](management-return-values.md).

## <a name="remarks"></a>Remarques

La fonction **SceSvcAttachmentAnalyze** doit effectuer les opérations suivantes :

-   Interroger directement les informations de configuration à partir du service.
-   Appelez la fonction de rappel vers laquelle pointe le membre **pfQueryInfo** de la structure d' [**\_ \_ informations de rappel SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) pour récupérer les informations de la base de données de sécurité.
-   Calcule les différences entre les informations en fonction du type et de la syntaxe.
-   Appelez la fonction de rappel vers laquelle pointe le membre **pfSetInfo** de la structure d' [**\_ \_ informations de rappel SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) pour mettre à jour la base de données de sécurité avec les informations de service récupérées différentes.

Pour plus d’informations, consultez [implémentation de SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).

## <a name="requirements"></a>Configuration requise



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

 

 




