---
description: 'Méthode IShellDispatch2. GetSystemInformation : récupère les informations système.'
ms.assetid: 57c066e3-080f-4ecc-b56e-877f0569e901
title: Méthode IShellDispatch2. GetSystemInformation (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a81ac091dc1905c1cbcd2c41575c907ce957e60c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117107"
---
# <a name="ishelldispatch2getsysteminformation-method"></a>Méthode IShellDispatch2. GetSystemInformation

Récupère des informations système.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = IShellDispatch2.GetSystemInformation(
  sName
)
```


```VB

IShellDispatch2.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*sName* \[ dans\]
</dt> <dd>

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Chaîne** qui spécifie les informations système demandées.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

### <a name="jscript"></a>JScript

Type : **variante**

Retourne la valeur des informations système demandées. Le type de retour dépend des informations système demandées. Pour plus d'informations, consultez la section Notes.

### <a name="vb"></a>VB

Type : **variante**

Retourne la valeur des informations système demandées. Le type de retour dépend des informations système demandées. Pour plus d'informations, consultez la section Notes.

## <a name="remarks"></a>Notes 

Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. GetSystemInformation**](./shell-getsysteminformation.md) .

Cette méthode peut être utilisée pour demander de nombreuses valeurs d’informations système. Le tableau suivant indique la valeur *sName* utilisée pour demander les informations et le type associé de la valeur retournée.



*sName*

Type de retour

Description

DirectoryServiceAvailable

**Booléen**

Affectez la valeur **true** si le service d’annuaire est disponible ; Sinon, **false**.

DoubleClickTime

**Integer**

Durée du double-clic, en millisecondes.

ProcessorLevel

**Integer**

**Windows Vista et versions ultérieures**. Niveau du processeur. Retourne 3, 4 ou 5 pour les processeurs de niveau x386, x486 et Pentium, respectivement.

ProcessorSpeed

**Integer**

Vitesse du processeur, en mégahertz (MHz).

ProcessorArchitecture

**Integer**

Architecture du processeur. Pour plus d’informations, consultez la description du membre **wProcessorArchitecture** de la structure des [**\_ informations système**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) .

PhysicalMemoryInstalled

**Integer**

Quantité de mémoire physique installée, en octets.

Les éléments suivants sont valides uniquement sur Windows XP.

Fichiers ISO \_ professionnel

**Booléen**

Définir sur **true** si le système d’exploitation est Windows XP Professionnel Edition ; Sinon, **false**.

Fichiers ISO \_ personnel

**Booléen**

Définir sur **true** si le système d’exploitation est Windows XP Édition personnelle ; Sinon, **false**.

Les éléments suivants sont valides uniquement sur Windows XP et versions ultérieures.

Fichiers ISO \_ MEMBRE_DOMAINE

**Booléen**

Défini sur **true** si l’ordinateur est membre d’un domaine ; Sinon, **false**.



 

Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.

## <a name="examples"></a>Exemples

Les exemples suivants illustrent l’utilisation de **GetSystemInformation** pour JScript et VBScript.

Langage


```JScript
<script language="JavaScript">
    function fnGetSystemInformationJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;

        vReturn = objShell.GetSystemInformation("ProcessorLevel");
        document.write(vReturn);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnGetSystemInformationVB()
        dim objShell
        dim vReturn

        set objShell = CreateObject("shell.application")

        vReturn = objShell.GetSystemInformation("ProcessorLevel")
        document.write(vReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



 

 
