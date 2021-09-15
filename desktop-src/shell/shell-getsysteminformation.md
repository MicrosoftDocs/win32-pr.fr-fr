---
description: Shell. GetSystemInformation, méthode-récupère les informations système.
ms.assetid: 94C10DD6-FE49-4dd4-AEED-69B73A75EDEF
title: Shell. GetSystemInformation, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b9e021e767309007cfee2cfc78268fb7d7cea042
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412398"
---
# <a name="shellgetsysteminformation-method"></a>Shell. GetSystemInformation, méthode

Récupère des informations système.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = Shell.GetSystemInformation(
  sName
)
```


```VB

Shell.GetSystemInformation( _
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

## <a name="return-value"></a>Valeur de retour

### <a name="jscript"></a>JScript

Type : **variante**

Retourne la valeur des informations système demandées. Le type de retour dépend des informations système demandées. Pour plus d'informations, consultez la section Notes.

### <a name="vb"></a>VB

Type : **variante**

Retourne la valeur des informations système demandées. Le type de retour dépend des informations système demandées. Pour plus d'informations, consultez la section Notes.

## <a name="remarks"></a>Notes

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

les éléments suivants sont valides uniquement sur Windows XP.

Fichiers ISO \_ Professional

**Booléen**

définir sur **true** si le système d’exploitation est Windows XP Professional Edition ; Sinon, **false**.

Fichiers ISO \_ personnel

**Booléen**

définir sur **true** si le système d’exploitation est Windows XP édition personnelle ; Sinon, **false**.

les éléments suivants sont valides uniquement sur Windows XP et versions ultérieures.

Fichiers ISO \_ MEMBRE_DOMAINE

**Booléen**

Défini sur **true** si l’ordinateur est membre d’un domaine ; Sinon, **false**.



 

Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.

## <a name="examples"></a>Exemples

les exemples suivants illustrent l’utilisation de **GetSystemInformation** pour JScript et VBScript.

JScript :


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



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



 

 
