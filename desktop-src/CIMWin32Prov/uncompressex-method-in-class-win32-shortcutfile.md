---
description: Décompresse le fichier de raccourci logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode decompress.
ms.assetid: aa1c04d1-4cce-4096-bce3-b9c61b9a4eb7
ms.tgt_platform: multiple
title: Méthode UncompressEx de la classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e07e86be3666b06063ef81c896eab6ee7a918657
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225228"
---
# <a name="uncompressex-method-of-the-win32_shortcutfile-class"></a>Méthode UncompressEx de la \_ classe Win32 ShortcutFile

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UncompressEx** décompresse le fichier de raccourci logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode [**decompress**](uncompress-method-in-class-win32-directory.md) .

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StopFileName* \[ à\]
</dt> <dd>

Nom du fichier ou du répertoire dans lequel la méthode **UncompressEx** a échoué. Ce paramètre a la **valeur null** si la méthode est réussie.

</dd> <dt>

*StartFileName* \[ dans, facultatif\]
</dt> <dd>

Nomme le fichier ou le répertoire enfant à utiliser comme point de départ pour **UncompressEx**. Le paramètre *StartFileName* est généralement le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent. Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de ExecMethod.

</dd> <dt>

*Récursif* \[ dans, facultatif\]
</dt> <dd>

Si la **valeur est true**, la modification de la propriété sera appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ LogicalFile**](cim-logicalfile.md) .

> [!Note]  
> Pour les instances de fichier, le paramètre *recursive* est ignoré.

 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la valeur 0 (zéro) si le fichier a été décompressé avec succès, et tout autre nombre pour indiquer une erreur.

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

[**\_ShortcutFile Win32**](win32-shortcutfile.md)
</dt> </dl>

 

