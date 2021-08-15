---
description: Vous pouvez obtenir ou modifier les données du Registre à l’aide de la classe WMI StdRegProv et de ses méthodes.
ms.assetid: 7cba9dcb-741b-4118-9769-8830c6dc0752
ms.tgt_platform: multiple
title: Obtention de données de Registre
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b904316809a6949c6897e32127f85569e3b2ac13cb769db4739e61c164aa19fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050637"
---
# <a name="obtaining-registry-data"></a>Obtention de données de Registre

Vous pouvez obtenir ou modifier les données du Registre à l’aide de la classe WMI [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) et de ses méthodes. Si vous utilisez l’utilitaire regedit pour afficher et modifier les valeurs de Registre sur l’ordinateur local, **StdRegProv** vous permet d’utiliser un script ou une application pour automatiser ces activités sur l’ordinateur local et les ordinateurs distants.

[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) contient des méthodes pour effectuer les opérations suivantes :

-   Vérifier les autorisations d’accès pour un utilisateur
-   Créer, énumérer et supprimer des clés de Registre
-   Créer, énumérer et supprimer des sous-clés ou des valeurs nommées
-   Lire, écrire et supprimer des valeurs de données

Les données du Registre sont organisées par sous-arborescences, clés et sous-clés imbriquées sous une clé de niveau supérieur. Les valeurs de données réelles sont appelées entrées ou valeurs nommées.

Les sous-arborescences sont les suivantes :

-   **HKEY \_ CLASSES \_ racine** (abrégées en **HKCR**)
-   **HKEY \_ \_utilisateur actuel** (**HKCU**)
-   **HKEY \_ \_ordinateur local** (**HKLM**)
-   **HKEY, \_ utilisateurs**
-   **configuration de HKEY \_ Current \_**

Par exemple, dans l’entrée de Registre **HKEY** \\ **Software** \\ **Microsoft** \\ **DirectX** \\ **InstalledVersion**, la sous-arborescence HKEY est **Software**; les sous-clés sont **Microsoft** et **DirectX**; et l’entrée de valeur nommée est **InstalledVersion**.

Un [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) se produit lorsqu’une modification apportée à une clé spécifique se produit, mais que l’entrée n’identifie pas la manière dont les valeurs sont modifiées et que cet événement est déclenché par des modifications sous la clé spécifiée. Pour identifier les modifications n’importe où dans une structure de clé hiérarchique, utilisez [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), qui ne retourne pas de valeurs spécifiques ou de modifications de clé qui se produisent. Pour obtenir une modification de valeur d’entrée spécifique, utilisez [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent), puis lisez l’entrée pour obtenir une valeur de ligne de base.

[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) possède uniquement des méthodes qui peuvent être appelées à partir de C++ ou d’un script, ce qui diffère de la structure de la classe Win32.

L’exemple de code suivant montre comment utiliser la méthode [**StdRegProv. enumKey**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) pour répertorier toutes les sous-clés logicielles Microsoft sous la clé de registre.

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft**


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650
$strKeyPath = &quot;SOFTWARE\Microsoft&quot;

$objReg = [WMIClass]&quot;root\default:StdRegProv&quot;

$arrSubKeys = $objReg.EnumKey($HKEY_LOCAL_MACHINE, $strKeyPath)
foreach ($subKey in ($arrSubKeys.sNames))
{
    $subKey
}
```





[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) a des méthodes différentes pour lire les différents types de données de valeur d’entrée de registre. Si l’entrée contient des valeurs inconnues, vous pouvez appeler [**StdRegProv. EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) pour les répertorier. Le tableau suivant répertorie la correspondance entre les méthodes **StdRegProv** et les types de données.



| Méthode                                                                                  | Type de données           |
|-----------------------------------------------------------------------------------------|---------------------|
| [**GetBinaryValue**](/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov)                 | **\_fichier binaire reg**     |
| [**GetDWORDValue**](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov)                   | **\_valeur DWORD reg**      |
| [**GetExpandedStringValue**](/previous-versions/windows/desktop/regprov/getexpandedstringvalue-method-in-class-stdregprov) | **REG \_ développer \_ SZ** |
| [**GetMultiStringValue**](/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov)       | **REG \_ multiple \_ SZ**  |
| [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov)                 | **SZ de REG \_**         |



 

Le tableau suivant répertorie les méthodes correspondantes pour la création de clés ou de valeurs, ou la modification de clés existantes.



| Méthode                                                                                  | Type de données           |
|-----------------------------------------------------------------------------------------|---------------------|
| [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov)                 | **\_fichier binaire reg**     |
| [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov)                   | **\_valeur DWORD reg**      |
| [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) | **REG \_ développer \_ SZ** |
| [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)       | **REG \_ multiple \_ SZ**  |
| [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)                 | **SZ de REG \_**         |



 

L’exemple suivant montre comment lire la liste des sources du journal des événements système à partir de la clé de registre.

**HKEY \_ Système d' \_ ordinateur local** système de \\  \\ contrôle des services du **jeu de contrôle actuel** \\  \\  \\ 

Notez que les éléments de la valeur multichaîne sont traités comme une collection ou un tableau.


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" _ 
    & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```



Le fournisseur de Registre est hébergé dans LocalService, et non dans le LocalSystem. Par conséquent, il n’est pas possible d’obtenir des informations à distance à partir de la sous-arborescence **HKEY \_ Current \_ User** . Toutefois, les scripts exécutés sur l’ordinateur local peuvent toujours accéder à **HKEY \_ Current \_ User**. Vous pouvez définir le modèle d’hébergement sur LocalSystem sur un ordinateur distant, mais cela pose un problème de sécurité, car le registre sur l’ordinateur distant est vulnérable à un accès hostile. Pour plus d’informations, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).

## <a name="examples"></a>Exemples

L’exemple de code VBScript [lire une valeur de Registre binaire](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) dans la Galerie TechNet utilise WMI pour lire une valeur de Registre binaire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tâches WMI : Registre](wmi-tasks--registry.md)
</dt> </dl>

 

 
