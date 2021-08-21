---
description: Copie le fichier ou le répertoire du codec logique spécifié dans le chemin de l’objet vers l’emplacement spécifié par le paramètre d’entrée.
ms.assetid: 77e67b01-561b-4233-899d-fa4bbf75ecf8
ms.tgt_platform: multiple
title: Méthode Copy de la classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2a7320e4e8474f88ac6721862b50b89534c098db74ac3dc844b50987cb08095d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504949"
---
# <a name="copy-method-of-the-win32_codecfile-class"></a>Méthode Copy de la \_ classe CodecFile Win32

La méthode **Copy** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) copie le fichier de codec logique ou le répertoire spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée. Une copie n’est pas prise en charge si le remplacement d’un fichier logique existant est nécessaire.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Copy(
   string FileName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FileName* 
</dt> <dd>

Nom complet de la copie du fichier (ou du répertoire). Exemple : c : \\ temp \\ newDirectory.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur 0 (zéro) si le fichier a été copié avec succès, et tout autre nombre pour indiquer une erreur.

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

[**\_CodecFile Win32**](win32-codecfile.md)
</dt> </dl>

 

