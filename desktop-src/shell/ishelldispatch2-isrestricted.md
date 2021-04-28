---
description: 'Méthode IShellDispatch2. IsRestricted : récupère le paramètre de restriction d’un groupe à partir du Registre.'
ms.assetid: 04275c5f-c3ed-4962-882f-2cce0258a9f4
title: Méthode IShellDispatch2. IsRestricted (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b4f482407fadd16d7ecfe9deeafd91b032a9a24f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117097"
---
# <a name="ishelldispatch2isrestricted-method"></a><span data-ttu-id="7c2ed-103">Méthode IShellDispatch2. IsRestricted</span><span class="sxs-lookup"><span data-stu-id="7c2ed-103">IShellDispatch2.IsRestricted method</span></span>

<span data-ttu-id="7c2ed-104">Récupère le paramètre de restriction d’un groupe à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-104">Retrieves a group's restriction setting from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c2ed-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c2ed-105">Syntax</span></span>


```JScript
iRetVal = IShellDispatch2.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

IShellDispatch2.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="7c2ed-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c2ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c2ed-107">*sGroup* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7c2ed-107">*sGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c2ed-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="7c2ed-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="7c2ed-109">**Chaîne** qui contient le nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-109">A **String** that contains the group name.</span></span> <span data-ttu-id="7c2ed-110">Cette valeur est le nom d’une sous-clé de Registre sous laquelle vérifier la restriction.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-110">This value is the name of a registry subkey under which to check for the restriction.</span></span>

</dd> <dt>

<span data-ttu-id="7c2ed-111">*sRestriction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7c2ed-111">*sRestriction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c2ed-112">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="7c2ed-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="7c2ed-113">**Chaîne** qui contient la restriction dont la valeur doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-113">A **String** that contains the restriction whose value is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c2ed-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7c2ed-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="7c2ed-115">JScript</span><span class="sxs-lookup"><span data-stu-id="7c2ed-115">JScript</span></span>

<span data-ttu-id="7c2ed-116">Type : **entier \***</span><span class="sxs-lookup"><span data-stu-id="7c2ed-116">Type: **Integer\***</span></span>

<span data-ttu-id="7c2ed-117">Valeur de la restriction.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-117">The value of the restriction.</span></span> <span data-ttu-id="7c2ed-118">Si la restriction spécifiée est introuvable, la valeur de retour est 0.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-118">If the specified restriction is not found, the return value is 0.</span></span>

### <a name="vb"></a><span data-ttu-id="7c2ed-119">VB</span><span class="sxs-lookup"><span data-stu-id="7c2ed-119">VB</span></span>

<span data-ttu-id="7c2ed-120">Type : **entier \***</span><span class="sxs-lookup"><span data-stu-id="7c2ed-120">Type: **Integer\***</span></span>

<span data-ttu-id="7c2ed-121">Valeur de la restriction.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-121">The value of the restriction.</span></span> <span data-ttu-id="7c2ed-122">Si la restriction spécifiée est introuvable, la valeur de retour est 0.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-122">If the specified restriction is not found, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c2ed-123">Notes </span><span class="sxs-lookup"><span data-stu-id="7c2ed-123">Remarks</span></span>

<span data-ttu-id="7c2ed-124">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. IsRestricted**](./shell-isrestricted.md) .</span><span class="sxs-lookup"><span data-stu-id="7c2ed-124">This method is implemented and accessed through the [**Shell.IsRestricted**](./shell-isrestricted.md) method.</span></span>

<span data-ttu-id="7c2ed-125">**IsRestricted** recherche d’abord un nom de sous-clé qui correspond à *sGroup* sous la clé suivante.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-125">**IsRestricted** first looks for a subkey name that matches *sGroup* under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

<span data-ttu-id="7c2ed-126">Les restrictions sont déclarées en tant que valeurs des sous-clés de stratégie individuelles.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-126">Restrictions are declared as values of the individual policy subkeys.</span></span> <span data-ttu-id="7c2ed-127">Si la restriction nommée dans *sRestriction* se trouve dans la sous-clé nommée dans *sGroup*, **IsRestricted** retourne la valeur actuelle de la restriction.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-127">If the restriction named in *sRestriction* is found in the subkey named in *sGroup*, **IsRestricted** returns the restriction's current value.</span></span> <span data-ttu-id="7c2ed-128">Si la restriction est introuvable sous **HKEY \_ local \_ machine**, la même sous-clé est vérifiée sous **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-128">If the restriction is not found under **HKEY\_LOCAL\_MACHINE**, the same subkey is checked under **HKEY\_CURRENT\_USER**.</span></span>

<span data-ttu-id="7c2ed-129">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-129">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="7c2ed-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="7c2ed-130">Examples</span></span>

<span data-ttu-id="7c2ed-131">Les exemples suivants illustrent l’utilisation de **IsRestricted** pour récupérer la valeur de données de la restriction **undockwithoutlogon** à partir de la sous-clé **système** .</span><span class="sxs-lookup"><span data-stu-id="7c2ed-131">The following examples show the use of **IsRestricted** to retrieve the data value of the **undockwithoutlogon** restriction from the **System** subkey.</span></span> <span data-ttu-id="7c2ed-132">L’utilisation est indiquée pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="7c2ed-132">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="7c2ed-133">Langage</span><span class="sxs-lookup"><span data-stu-id="7c2ed-133">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsRestricedJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var lReturn;
        
        lReturn = objShell.IsRestricted("system", "undockwithoutlogon");
        document.write(lReturn);
    }
</script>
```



<span data-ttu-id="7c2ed-134">VBScript</span><span class="sxs-lookup"><span data-stu-id="7c2ed-134">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsRestricedVB()
        dim objShell
        dim lReturn

        set objShell = CreateObject("shell.application")

        lReturn = objShell.IsRestricted("system", "undockwithoutlogon")
        document.write(lReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="7c2ed-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c2ed-135">Requirements</span></span>



| <span data-ttu-id="7c2ed-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c2ed-136">Requirement</span></span> | <span data-ttu-id="7c2ed-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c2ed-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c2ed-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c2ed-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7c2ed-139">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c2ed-139">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7c2ed-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c2ed-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7c2ed-141">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7c2ed-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7c2ed-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c2ed-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c2ed-143"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c2ed-143"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="7c2ed-144">MIDL</span><span class="sxs-lookup"><span data-stu-id="7c2ed-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7c2ed-145"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7c2ed-145"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="7c2ed-146">DLL</span><span class="sxs-lookup"><span data-stu-id="7c2ed-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c2ed-147"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="7c2ed-147"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
