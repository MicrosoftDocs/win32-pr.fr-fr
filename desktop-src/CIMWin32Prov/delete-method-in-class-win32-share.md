---
description: Supprime un nom de partage de la liste des ressources partagées d’un serveur, en déconnectant les connexions à la ressource partagée.
ms.assetid: 175f9c0e-0017-4a86-8e05-ad78e2c93c11
ms.tgt_platform: multiple
title: Méthode Delete de la classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2048ba9dac91b139888f27c037d64849de8a4ee8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999525"
---
# <a name="delete-method-of-the-win32_share-class"></a>Méthode Delete de la \_ classe de partage Win32

La méthode **Delete** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) supprime un nom de partage de la liste des ressources partagées d’un serveur, en déconnectant les connexions à la ressource partagée.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Delete();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

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

## <a name="remarks"></a>Notes

La méthode **Delete** est une méthode d’objet qui est utilisée sur une instance d’une classe.

Seuls les membres du groupe local Administrateurs ou opérateurs de compte ou ceux ayant une appartenance de groupe communication, impression ou opérateur de serveur peuvent exécuter la méthode avec succès. L’opérateur Print peut uniquement supprimer des files d’attente d’impression. L’opérateur de communication peut supprimer uniquement les files d’attente de communication des appareils.

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant supprime le partage spécifié.


```VB
On Error Resume Next

ComputerName = InputBox("Enter the computer name:", "Delete Share", "localhost")

SName = InputBox("Enter the name of the share:", "Delete Share")



Set Shares = GetObject("winmgmts:\\" & ComputerName & _
 "\root\cimv2").ExecQuery("SELECT * FROM Win32_Share WHERE name = '" & SName & "'")



For Each Share in Shares
 Share.Delete()
Next
```



L’exemple de code PowerShell suivant supprime les partages vides.


```PowerShell
$Shares = Get-WMIObject Win32_Share | Where {$_.Name -eq ""}

Foreach ($Share in $Shares) {
   $Share.Delete()
}
"{0} blank shares found and removed" -f $shares.count
```



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

[**\_Partage Win32**](win32-share.md)
</dt> </dl>

 

