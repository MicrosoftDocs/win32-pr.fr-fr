---
description: SetShareInfo&\# 8194 ; La méthode de classe WMI définit les paramètres d’une ressource partagée.
ms.assetid: f6379261-9325-4b7f-92df-438c5029569f
ms.tgt_platform: multiple
title: Méthode SetShareInfo de la classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb9ee76a0b8336ccdca90a04ee3c2a223b7269a30a00276418d6c46a8bb3abc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800899"
---
# <a name="setshareinfo-method-of-the-win32_share-class"></a>Méthode SetShareInfo de la \_ classe de partage Win32

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetShareInfo** définit les paramètres d’une ressource partagée.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

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

Exemple : 10. Ce paramètre est facultatif.

</dd> <dt>

*Description* \[ dans, facultatif\]
</dt> <dd>

Commentaire facultatif pour décrire la ressource partagée.

</dd> <dt>

*Accès* \[ dans, facultatif\]
</dt> <dd>

Descripteur de sécurité pour les autorisations au niveau de l’utilisateur. Un descripteur de sécurité contient des informations sur l’autorisation, le propriétaire et les capacités d’accès de la ressource. Pour plus d’informations, [**consultez \_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs répertoriées dans la liste suivante ou toute autre valeur pour indiquer une erreur.

<dl> <dt>

**Opération réussie** (0)
</dt> <dt>

**Accès refusé** (2)
</dt> <dt>

**Échec inconnu** (8)
</dt> <dt>

**Nom non valide** (9)
</dt> <dt>

**Niveau non valide** (10)
</dt> <dt>

**Paramètre non valide** (21)
</dt> <dt>

**Partage en double** (22)
</dt> <dt>

**Chemin d’accès Redirigé** (23)
</dt> <dt>

**Périphérique ou répertoire inconnu** (24)
</dt> <dt>

**Nom de réseau introuvable** (25)
</dt> <dt>

**Autre** (26 4294967295)
</dt> </dl>

## <a name="remarks"></a>Remarques

La méthode **SetShareInfo** est une méthode d’objet dynamique qui est utilisée sur une occurrence de cette classe.

Seuls les membres du groupe local Administrateurs ou opérateurs de compte ou ceux ayant une appartenance de groupe communication, impression ou opérateur de serveur peuvent exécuter **SetShareInfo**. L’opérateur Print peut uniquement définir des files d’attente d’impression. L’opérateur de communication ne peut définir que des files d’attente d’appareils de communication.

## <a name="examples"></a>Exemples

L’exemple PowerShell suivant met à jour le nom du partage **newShare** .


```PowerShell
$newShare = Get-WmiObject win32_share | Where-Object {$_.name -eq "newShare"}
[void]$newShare.SetShareInfo($null,"This is my new description",$null)
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Partage Win32**](win32-share.md)
</dt> </dl>

 

