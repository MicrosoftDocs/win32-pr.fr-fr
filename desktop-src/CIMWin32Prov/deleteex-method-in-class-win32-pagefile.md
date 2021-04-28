---
description: 'Méthode DeleteEx de la classe Win32_PageFile : supprime le fichier d’échange logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.'
ms.assetid: ea31f92a-94b9-4d4d-abd9-6c304ac5caee
ms.tgt_platform: multiple
title: Méthode DeleteEx de la classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 34e27e80c3cfaea352ee97ad29aed0b7ca358546
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097047"
---
# <a name="deleteex-method-of-the-win32_pagefile-class"></a>Méthode DeleteEx de la \_ classe du fichier d’échange Win32

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **DeleteEx** supprime le fichier d’échange logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. **DeleteEx** est une version étendue de la méthode [**Delete**](delete-method-in-class-win32-directory.md) .

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StopFileName* \[ à\]
</dt> <dd>

Nom du fichier ou du répertoire dans lequel la méthode **DeleteEx** a échoué. Ce paramètre a la **valeur null** si la méthode est réussie.

</dd> <dt>

*StartFileName* \[ dans, facultatif\]
</dt> <dd>

Nomme le fichier ou le répertoire enfant à utiliser comme point de départ pour **DeleteEx**. Le paramètre *StartFileName* est généralement le paramètre *StopFileName* qui spécifie le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent. Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de ExecMethod.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la valeur 0 (zéro) si le fichier a été supprimé avec succès, et tout autre nombre pour indiquer une erreur.

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

[**\_Fichier d’échange Win32**](win32-pagefile.md)
</dt> </dl>

 

