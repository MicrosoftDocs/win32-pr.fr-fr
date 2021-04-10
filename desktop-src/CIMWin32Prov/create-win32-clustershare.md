---
description: Crée une instance de \_ ClusterShare Win32.
ms.assetid: a6fde28d-f19e-4a31-8f0d-35927c75a030
ms.tgt_platform: multiple
title: Créer une méthode de la classe Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7cbf7c42b8523bcd12b19e9b474ecc50bd031939
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111534"
---
# <a name="create-method-of-the-win32_clustershare-class"></a>Créer une méthode de la \_ classe ClusterShare Win32

Crée une instance [**de \_ ClusterShare Win32**](win32-clustershare.md) .

## <a name="syntax"></a>Syntaxe


```mof
static uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Chemin d’accès* \[ dans\]
</dt> <dd>

Chemin d’accès local du partage Windows.

Par exemple, « C : \\ Program Files ».

</dd> <dt>

*Nom* \[ dans\]
</dt> <dd>

Alias d’un chemin d’accès configuré en tant que partage sur un système informatique exécutant Windows.

Exemple : « public ».

</dd> <dt>

*Type* \[ dans\]
</dt> <dd>

Type de ressource partagée. Les types sont les suivants : lecteurs de disque, files d’attente à l’impression, communications interprocessus (IPC) et périphériques généraux.

<dt>

0 (0x0)
</dt> <dd>

Lecteur de disque

</dd> <dt>

1 (0x1)
</dt> <dd>

File d'attente d'impression

</dd> <dt>

2 (0X2)
</dt> <dd>

Appareil

</dd> <dt>

3 (0x3)
</dt> <dd>

IPC

</dd> <dt>

2147483648 (0x80000000)
</dt> <dd>

Administrateur du lecteur de disque

</dd> <dt>

2147483649 (0x80000001)
</dt> <dd>

Administrateur de file d’attente à l’impression

</dd> <dt>

2147483650 (0x80000002)
</dt> <dd>

Administrateur de l’appareil

</dd> <dt>

2147483651 (0x80000003)
</dt> <dd>

Administrateur IPC

</dd> </dl> </dd> <dt>

*MaximumAllowed* \[ dans, facultatif\]
</dt> <dd>

Limite du nombre maximal d’utilisateurs autorisés à utiliser cette ressource simultanément.

</dd> <dt>

*Description* \[ dans, facultatif\]
</dt> <dd>

Description de l’objet.

</dd> <dt>

*Mot de passe* \[ dans, facultatif\]
</dt> <dd>

TBD

</dd> <dt>

*Accès* \[ dans, facultatif\]
</dt> <dd>

Instance incorporée facultative d’une classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) qui contient le descripteur de sécurité pour le nouveau partage.

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

 

