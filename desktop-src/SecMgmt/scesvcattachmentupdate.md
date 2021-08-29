---
description: La fonction SceSvcAttachmentUpdate est appelée par les composants logiciels enfichables de configuration de la sécurité pour transmettre les modifications de configuration à la base de données de sécurité.
ms.assetid: 2b5b3718-8ccb-480a-97fb-c8115d8f3a5c
title: SceSvcAttachmentUpdate fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentUpdate
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b04d8a144373ae493a956e2166ea6dab34d844c71504f303766e8de7915b9a70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004867"
---
# <a name="scesvcattachmentupdate-callback-function"></a>SceSvcAttachmentUpdate fonction de rappel

La fonction **SceSvcAttachmentUpdate** est appelée par les composants logiciels enfichables de configuration de la sécurité pour transmettre les modifications de configuration à la base de données de sécurité.

## <a name="syntax"></a>Syntaxe


```C++
SCESTATUS WINAPI SceSvcAttachmentUpdate(
  _In_ PSCESVC_CALLBACK_INFO     pSceCbInfo,
  _In_ SCESVC_CONFIGURATION_INFO *ServiceInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSceCbInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure d' [**\_ \_ informations de rappel SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) qui contient le handle de rappel et les pointeurs de fonction vers SCE.

</dd> <dt>

*ServiceInfo* \[ dans\]
</dt> <dd>

Informations de configuration mises à jour. La structure de données utilisée pour ces informations [**est \_ SCESVC \_ informations de configuration**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette fonction réussit, elle retourne SCESTATUS \_ Success. Sinon, elle retourne un code d’erreur. Pour plus d’informations sur les codes d’erreur de configuration de la sécurité, consultez [Attachment Return values](management-return-values.md).

## <a name="remarks"></a>Remarques

La fonction **SceSvcAttachmentUpdate** doit effectuer les opérations suivantes :

-   Appelez la fonction de rappel vers laquelle pointe le membre **pfQueryInfo** de la structure d' [**\_ \_ informations de rappel SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) pour récupérer les informations de configuration de base actuelles de la base de données de sécurité.
-   Appelez la fonction de rappel vers laquelle pointe le membre **pfQueryInfo** de la structure d' [**\_ \_ informations de rappel SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) pour récupérer le dernier jeu de différences (informations d’analyse) de la base de données de sécurité.
-   Utilisez les informations de service fournies (voir *serviceInfo*) pour calculer la nouvelle configuration de base.
-   Utilisez les informations de service fournies (voir *serviceInfo*) et l’analyse pour calculer les nouvelles informations relatives aux différences.
-   Appelez la fonction de rappel vers laquelle pointe le membre **pfSetInfo** de la structure d' [**\_ \_ informations de rappel SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) pour définir la nouvelle configuration de base dans la base de données de sécurité.
-   Appelez la fonction de rappel vers laquelle pointe le membre **pfSetInfo** de la structure d' [**\_ \_ informations de rappel SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) pour définir les nouvelles informations d’analyse dans la base de données de sécurité.

Pour plus d’informations, consultez [implémentation de SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_informations de rappel SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**\_informations de configuration de SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info)
</dt> </dl>

 

 




