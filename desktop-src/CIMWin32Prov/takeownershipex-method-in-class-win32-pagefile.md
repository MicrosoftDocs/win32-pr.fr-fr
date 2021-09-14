---
description: Obtient la propriété du fichier de pagination logique spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode TakeOwnerShip.
ms.assetid: 6c359910-713a-441e-b2e1-949929c07e93
ms.tgt_platform: multiple
title: Méthode TakeOwnerShipEx de la classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b0f4662b4884da227a64768cc29bce4c615f8f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010193"
---
# <a name="takeownershipex-method-of-the-win32_pagefile-class"></a>Méthode TakeOwnerShipEx de la \_ classe du fichier d’échange Win32

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShipEx** obtient la propriété du fichier de pagination logique spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode [**TakeOwnership**](takeownership-method-in-class-win32-directory.md) . Si le fichier logique est effectivement un répertoire, cette méthode agit de manière récursive, en prenant possession de tous les fichiers et sous-répertoires contenus dans le répertoire.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StopFileName* \[ à\]
</dt> <dd>

Nom du fichier ou du répertoire dans lequel la méthode **TakeOwnerShipEx** a échoué. Ce paramètre a la **valeur null** si la méthode est réussie.

</dd> <dt>

*StartFileName* \[ dans, facultatif\]
</dt> <dd>

Nomme le fichier ou le répertoire enfant à utiliser comme point de départ pour **TakeOwnerShipEx**. Le paramètre *StartFileName* est généralement le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent. Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de ExecMethod.

</dd> <dt>

*Récursif* \[ dans, facultatif\]
</dt> <dd>

Si la **valeur est true**, la modification de la propriété sera appliquée de manière récursive aux fichiers et répertoires dans le répertoire spécifié par l’instance [**CIM \_ LogicalFile**](cim-logicalfile.md) .

> [!Note]  
> Pour les instances de fichier, le paramètre *recursive* est ignoré.

 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.

<dl> <dt>

**0**
</dt> <dd>

La demande a abouti.

</dd> <dt>

**2**
</dt> <dd>

L’accès a été refusé.

</dd> <dt>

**8**
</dt> <dd>

Une erreur non spécifiée s’est produite.

</dd> <dt>

**9**
</dt> <dd>

Le nom spécifié n’est pas valide.

</dd> <dt>

**10**
</dt> <dd>

L’objet spécifié existe déjà.

</dd> <dt>

**11**
</dt> <dd>

Le système de fichiers n’est pas NTFS.

</dd> <dt>

**12**
</dt> <dd>

La plateforme n’est pas Windows.

</dd> <dt>

**13**
</dt> <dd>

Le lecteur n’est pas le même.

</dd> <dt>

**14**
</dt> <dd>

Le répertoire n'est pas vide.

</dd> <dt>

**15**
</dt> <dd>

Une violation de partage s’est produite.

</dd> <dt>

**16**
</dt> <dd>

Le fichier de démarrage spécifié n’est pas valide.

</dd> <dt>

**17**
</dt> <dd>

Un privilège requis pour l’opération n’est pas conservé.

</dd> <dt>

**21**
</dt> <dd>

Un paramètre spécifié n’est pas valide.

</dd> </dl>

## <a name="requirements"></a>Spécifications



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

[**\_Fichier d’échange Win32**](win32-pagefile.md)
</dt> </dl>

 

