---
description: La méthode GetAccessMask de la classe Win32_Share-retourne une bitmap UInt32 avec les droits d’accès au partage détenu par l’utilisateur ou le groupe au nom duquel l’instance est retournée.
ms.assetid: 234f44a4-ffff-431d-a973-98f2bd313c7d
ms.tgt_platform: multiple
title: Méthode GetAccessMask de la classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.GetAccessMask
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ebc2b2620b0bdc019e117f9a4b2c376be6320be968fdae42509dc3f62c3cc9a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077659"
---
# <a name="getaccessmask-method-of-the-win32_share-class"></a>Méthode GetAccessMask de la \_ classe de partage Win32

La méthode **GetAccessMask** retourne une bitmap UInt32 avec les droits d’accès au partage détenu par l’utilisateur ou le groupe au nom duquel l’instance est retournée.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Droits d’accès au partage détenu par l’utilisateur ou le groupe.

<dl> <dt>

**\_Répertoire de liste de fichiers \_**
</dt> <dd>

1 (0x1)

Accorde le droit de lire des données à partir du fichier. Pour un répertoire, cette valeur accorde le droit de répertorier le contenu du répertoire.

</dd> <dt>

**fichier \_ ajouter \_ un fichier**
</dt> <dd>

2 (0X2)

Accorde le droit d’écrire des données dans le fichier. Pour un répertoire, cette valeur accorde le droit de créer un fichier dans le répertoire.

</dd> <dt>

**FICHIER \_ Ajouter un \_ sous-répertoire**
</dt> <dd>

4 (0x4)

Accorde le droit d’ajouter des données au fichier. Pour un répertoire, cette valeur accorde le droit de créer un sous-répertoire.

</dd> <dt>

**lecture de fichier \_ \_ EA**
</dt> <dd>

8 (0x8)

Accorde le droit de lire les attributs étendus.

</dd> <dt>

**écriture de fichier \_ \_ EA**
</dt> <dd>

16 (0x10)

Accorde le droit d’écrire des attributs étendus.

</dd> <dt>

**parcours de fichiers \_**
</dt> <dd>

32 (0x20)

Accorde le droit d’exécuter un fichier. Pour un répertoire, le répertoire peut être parcouru.

</dd> <dt>

**\_supprimer un \_ enfant de fichier**
</dt> <dd>

64 (0x40)

Accorde le droit de supprimer un répertoire et tous les fichiers qu’il contient (ses enfants), même si les fichiers sont en lecture seule.

</dd> <dt>

**\_attributs de lecture de fichier \_**
</dt> <dd>

128 (0x80)

Accorde le droit de lire les attributs du fichier.

</dd> <dt>

**\_attributs d’écriture de fichier \_**
</dt> <dd>

256 (0x100)

Accorde le droit de modifier les attributs de fichier.

</dd> <dt>

**DELETE**
</dt> <dd>

65536 (0x10000)

Octroie l’accès en suppression.

</dd> <dt>

**LIRE \_ le contrôle**
</dt> <dd>

131072 (0x20000)

Octroie l’accès en lecture au descripteur de sécurité et au propriétaire.

</dd> <dt>

**ÉCRITURE \_ DAC**
</dt> <dd>

262144 (0x40000)

Accorde un accès en écriture à la liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List).

</dd> <dt>

**propriétaire en écriture \_**
</dt> <dd>

524288 (0x80000)

Affecte le propriétaire de l’écriture.

</dd> <dt>

**NON**
</dt> <dd>

1048576 ()

Synchronise l’accès et permet à un processus d’attendre qu’un objet passe à l’état signalé.

</dd> </dl>

## <a name="remarks"></a>Remarques

La méthode **GetAccessMask** est une méthode d’objet qui est utilisée sur une occurrence de cette classe.

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant crée un dossier de partage, puis obtient la valeur du masque d’accès dans le descripteur de sécurité qui sécurise le dossier de partage.


```VB
Const FILE_SHARE = 0
Const MAXIMUM_CONNECTIONS = 4000 
strComputer = "."

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objNewShare = objWMIService.Get("Win32_Share")
Return = objNewShare.Create ("C:\Temp", "TestShare", FILE_SHARE, MAXIMUM_CONNECTIONS, "test share")

If Return <> 0 Then
          WScript.Echo Return
          WScript.Quit
End If

Set objShare = objWMIService.Get("Win32_Share.Name='TestShare'")
Return = objShare.GetAccessMask
WScript.Echo Return
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

[**\_Partage Win32**](win32-share.md)
</dt> </dl>

 

