---
description: Définit les paramètres de la ressource partagée.
ms.assetid: 592d0fa6-c865-4f70-89c3-b58204a8c5a6
ms.tgt_platform: multiple
title: Méthode SetShareInfo de la classe Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 07245e97e091f607d142de57c00109d3671bd81b5f34b9062681229090ff6b50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439399"
---
# <a name="setshareinfo-method-of-the-win32_clustershare-class"></a>Méthode SetShareInfo de la \_ classe Win32 ClusterShare

Définit les paramètres de la ressource partagée.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*MaximumAllowed* \[ dans, facultatif\]
</dt> <dd>

Limite du nombre maximal d’utilisateurs autorisés à utiliser cette ressource simultanément.

</dd> <dt>

*Description* \[ dans, facultatif\]
</dt> <dd>

Décrit la ressource partagée.

</dd> <dt>

*Accès* \[ dans, facultatif\]
</dt> <dd>

Descripteur de sécurité pour les autorisations au niveau de l’utilisateur. Un descripteur de sécurité contient des informations sur l’autorisation, le propriétaire et les capacités d’accès de la ressource. Pour plus d’informations, [**consultez \_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                       |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ClusterShare Win32**](win32-clustershare.md)
</dt> </dl>

 

