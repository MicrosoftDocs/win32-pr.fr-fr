---
description: 'La classe de fournisseur de Registre système StdRegProv pour WMI a des méthodes qui effectuent les opérations suivantes :'
ms.assetid: d42248b3-2f96-4771-aee9-a0db139b149e
ms.tgt_platform: multiple
title: Modification des données de Registre
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b51f3f18eb718dab7c79f31a4b2188dd7afa529
ms.sourcegitcommit: 3d9eb6638763fee8b87c378657458f814182e36c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106545198"
---
# <a name="changing-registry-data"></a><span data-ttu-id="6f664-103">Modification des données de Registre</span><span class="sxs-lookup"><span data-stu-id="6f664-103">Changing Registry Data</span></span>

<span data-ttu-id="6f664-104">La classe de [fournisseur de Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider) [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) pour WMI a des méthodes qui effectuent les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f664-104">The [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) class [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) for WMI has methods that do the following:</span></span>

-   <span data-ttu-id="6f664-105">Créez ou supprimez des clés de registre.</span><span class="sxs-lookup"><span data-stu-id="6f664-105">Create or delete registry keys.</span></span>

    <span data-ttu-id="6f664-106">Utilisez [**CreateKey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) ou [**DeleteKey**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov).</span><span class="sxs-lookup"><span data-stu-id="6f664-106">Use [**CreateKey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) or [**DeleteKey**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov).</span></span>

-   <span data-ttu-id="6f664-107">Créez ou supprimez des valeurs nommées, appelées entrées lorsqu’elles sont sous clés.</span><span class="sxs-lookup"><span data-stu-id="6f664-107">Create or delete named values, which are called entries when they are under keys.</span></span>

    <span data-ttu-id="6f664-108">Utilisez le nom d’une nouvelle valeur et [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov), [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov), [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov), [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)ou [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) pour créer une valeur nommée.</span><span class="sxs-lookup"><span data-stu-id="6f664-108">Use the name of a new value and [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov), [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov), [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov), [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov), or [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) to create a named value.</span></span> <span data-ttu-id="6f664-109">Utilisez [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) pour supprimer une valeur nommée.</span><span class="sxs-lookup"><span data-stu-id="6f664-109">Use [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) to delete a named value.</span></span>

-   <span data-ttu-id="6f664-110">Modifiez les valeurs nommées.</span><span class="sxs-lookup"><span data-stu-id="6f664-110">Change named values.</span></span>

    <span data-ttu-id="6f664-111">Utilisez le nom d’une valeur et les méthodes définies (identifiées dans l’élément à puce précédent) pour modifier les valeurs nommées existantes sous une clé.</span><span class="sxs-lookup"><span data-stu-id="6f664-111">Use the name of a value and the Set methods (identified in the previous bulleted item) to change existing named values under a key.</span></span> <span data-ttu-id="6f664-112">Vous devez connaître le nom d’une valeur pour la modifier.</span><span class="sxs-lookup"><span data-stu-id="6f664-112">You must know the name of a value to change it.</span></span> <span data-ttu-id="6f664-113">Si vous ne connaissez pas les noms de valeur sous une clé, utilisez la méthode [**EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) pour obtenir les noms.</span><span class="sxs-lookup"><span data-stu-id="6f664-113">If you do not know the value names under a key, use the [**EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) method to obtain the names.</span></span>

<span data-ttu-id="6f664-114">Les sections suivantes sont présentées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="6f664-114">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="6f664-115">Création d’une clé de Registre à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="6f664-115">Creating a Registry Key Using VBScript</span></span>](#creating-a-registry-key-using-vbscript)
-   [<span data-ttu-id="6f664-116">Création d’une valeur de Registre nommée à l’aide de PowerShell et VBScript</span><span class="sxs-lookup"><span data-stu-id="6f664-116">Creating a Named Registry Value Using PowerShell and VBScript</span></span>](#creating-a-named-registry-value-using-powershell-and-vbscript)

## <a name="creating-a-registry-key-using-vbscript"></a><span data-ttu-id="6f664-117">Création d’une clé de Registre à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="6f664-117">Creating a Registry Key Using VBScript</span></span>

<span data-ttu-id="6f664-118">Étant donné que le Registre est la base de données de configuration centrale pour le système d’exploitation, les applications et les services, soyez prudent lorsque vous écrivez des modifications apportées à des valeurs de registre ou supprimez des clés.</span><span class="sxs-lookup"><span data-stu-id="6f664-118">Because the registry is the central configuration database for the operating system, applications, and services, use caution when you write changes to registry values or delete keys.</span></span>

> [!Note]  
> <span data-ttu-id="6f664-119">Vous ne pouvez pas surveiller la sous-clé **\_ \_ racine HKEY classes** de **HKEY \_ Current \_ User (HKCU)**.</span><span class="sxs-lookup"><span data-stu-id="6f664-119">You cannot monitor the **HKEY\_CLASSES\_ROOT** subkey of **HKEY\_CURRENT\_USER(HKCU)**.</span></span> <span data-ttu-id="6f664-120">La surveillance des **\_ utilisateurs HKEY** n’est pas recommandée, car les sous-clés apparaissent et disparaissent au fur et à mesure que les ruches sont chargées.</span><span class="sxs-lookup"><span data-stu-id="6f664-120">Monitoring **HKEY\_USERS** is not recommended because the subkeys appear and disappear as hives are loaded.</span></span>

 

<span data-ttu-id="6f664-121">Les exemples de code suivants montrent comment créer une nouvelle clé de Registre et une sous-clé.</span><span class="sxs-lookup"><span data-stu-id="6f664-121">The following code examples show how to create a new registry key and a subkey.</span></span>


```VB
HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set ObjRegistry = GetObject("winmgmts:{impersonationLevel = impersonate}!\\" & strComputer & "\root\default:StdRegProv")

strPath = "SOFTWARE\MyKey\MySubKey"

Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

If Return <> 0 Then
    WScript.Echo "The operation failed." & Err.Number
    WScript.Quit
Else
    wScript.Echo "New registry key created" & VBCRLF & "HKLM\SOFTWARE\MYKey\"

End If
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650 
$strComputer = "."
$strPath = "SOFTWARE\MyKey\MySubKey"

$reg = [wmiclass]"\\$strComputer\root\default:StdRegprov"

[void]$reg.CreateKey($HKEY_LOCAL_MACHINE, $strPath)
```





## <a name="creating-a-named-registry-value-using-powershell-and-vbscript"></a><span data-ttu-id="6f664-122">Création d’une valeur de Registre nommée à l’aide de PowerShell et VBScript</span><span class="sxs-lookup"><span data-stu-id="6f664-122">Creating a Named Registry Value Using PowerShell and VBScript</span></span>

<span data-ttu-id="6f664-123">L’exemple de code suivant montre comment créer une valeur nommée appelée **MultiStringValue** sous la clé **HKEY \_ local \_ machine** \\ **Software** \\ **MyKey** \\ **MySubKey** créée par le script précédent.</span><span class="sxs-lookup"><span data-stu-id="6f664-123">The following code example shows how to create a named value called **MultiStringValue** under the **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**MyKey**\\**MySubKey** key that the previous script creates.</span></span> <span data-ttu-id="6f664-124">Le script appelle [**StdRegProv. SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) pour écrire des valeurs de chaîne dans une nouvelle valeur nommée.</span><span class="sxs-lookup"><span data-stu-id="6f664-124">The script calls [**StdRegProv.SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) to write string values to a new named value.</span></span>


```VB
const HKEY_LOCAL_MACHINE = &H80000002 
strComputer = "."

Set objRegistry = _
    GetObject("winmgmts:{impersonationLevel=impersonate}!\\" _ 
    & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\MyKey\MySubKey"
strValueName = "MultiStringValue"
arrStringValues = Array("one", "two","three", "four")

objRegistry.SetMultiStringValue HKEY_LOCAL_MACHINE, strKeyPath,_
    strValueName, arrStringValues

' Read the values that were just written
objRegistry.GetMultiStringValue HKEY_LOCAL_MACHINE, strKeyPath,_
    strValueName, arrStringValues   

For Each strValue in arrStringValues
    WScript.Echo strValue 
Next
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650 
$strComputer = "."
$strPath = "SOFTWARE\MyKey\MySubKey"

$strValueName = "MultiStringValue"
$arrStringValues = @("one", "two","three", "four")

$reg = [wmiclass]"\\$strComputer\root\default:StdRegprov"

[void]$reg.SetMultiStringValue($HKEY_LOCAL_MACHINE, $strKeyPath, $strValueName, $arrStringValues)

$multiValues = $reg.GetMultiStringValue($HKEY_LOCAL_MACHINE, $strKeyPath, $strValueName)
$multiValues.sValue
```

<span data-ttu-id="6f664-125">À l’aide de WMI, vous ne pouvez pas définir la sécurité d’accès sur une clé de registre.</span><span class="sxs-lookup"><span data-stu-id="6f664-125">Using WMI, you cannot set access security on a registry key.</span></span> <span data-ttu-id="6f664-126">Toutefois, la méthode [**StdRegProv. CheckAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) compare les paramètres de sécurité de l’utilisateur actuel au descripteur de sécurité sur une clé de Registre pour déterminer si l’utilisateur dispose d’une autorisation spécifique, telle que la **valeur du \_ jeu \_ de clés**.</span><span class="sxs-lookup"><span data-stu-id="6f664-126">However, the [**StdRegProv.CheckAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) method compares the security settings of the current user to the security descriptor on a registry key to determine if the user has a specific permission, such as **KEY\_SET\_VALUE**.</span></span>
