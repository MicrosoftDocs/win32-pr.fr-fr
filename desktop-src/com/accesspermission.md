---
title: AccessPermission
description: Décrit la liste de Access Control (ACL) des principaux qui peuvent accéder aux instances de cette classe. Cette liste de contrôle d’accès est utilisée uniquement par les applications qui n’appellent pas CoInitializeSecurity.
ms.assetid: 92518de0-66ca-4d7a-8d91-63b41e6d3c24
keywords:
- Valeur de Registre AccessPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6210eba77f614b16c8fde59948b350ad150909
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363388"
---
# <a name="accesspermission"></a>AccessPermission

Décrit la liste de Access Control (ACL) des principaux qui peuvent accéder aux instances de cette classe. Cette liste de contrôle d’accès est utilisée uniquement par les applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AccessPermission = ACL
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur **\_ binaire de Reg** . Il contient des données décrivant la liste de Access Control (ACL) des principaux qui peuvent accéder aux instances de cette classe. Lors de la réception d’une demande de connexion à un objet existant de cette classe, la liste de contrôle d’accès est vérifiée par l’application appelée en usurpant l’identité de l’appelant. Si la vérification de l’accès échoue, la connexion n’est pas autorisée. Si cette valeur nommée n’existe pas, la liste de contrôle d’accès [**DefaultAccessPermission**](defaultaccesspermission.md) est testée pour déterminer si la connexion doit être autorisée.

Pour les applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou n’utilisent pas l’interface [**IGlobalOptions**](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions) pour spécifier l’AppID, l’exécutable du binaire de l’application doit être mappé à l’AppID de l’application, comme décrit dans [**AppID**](appid.md). Cela est nécessaire pour que COM puisse localiser l’AppID de l’application.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**DefaultAccessPermission**](defaultaccesspermission.md)
</dt> <dt>

[Sécurité dans COM](security-in-com.md)
</dt> </dl>

 

 