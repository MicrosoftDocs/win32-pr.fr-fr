---
description: 'Méthode Shell. IsRestricted : récupère le paramètre de restriction d’un groupe à partir du Registre.'
ms.assetid: C4B3B5C0-7445-483a-885F-5283BD4D4B39
title: Shell. IsRestricted, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3e428c914cf95d282fd721071009efc70fcb3a4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104257"
---
# <a name="shellisrestricted-method"></a><span data-ttu-id="fbfbc-103">Shell. IsRestricted, méthode</span><span class="sxs-lookup"><span data-stu-id="fbfbc-103">Shell.IsRestricted method</span></span>

<span data-ttu-id="fbfbc-104">Récupère le paramètre de restriction d’un groupe à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-104">Retrieves a group's restriction setting from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbfbc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbfbc-105">Syntax</span></span>


```JScript
iRetVal = Shell.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

Shell.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="fbfbc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fbfbc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbfbc-107">*sGroup* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fbfbc-107">*sGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbfbc-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="fbfbc-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="fbfbc-109">**Chaîne** qui contient le nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-109">A **String** that contains the group name.</span></span> <span data-ttu-id="fbfbc-110">Cette valeur est le nom d’une sous-clé de Registre sous laquelle vérifier la restriction.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-110">This value is the name of a registry subkey under which to check for the restriction.</span></span>

</dd> <dt>

<span data-ttu-id="fbfbc-111">*sRestriction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fbfbc-111">*sRestriction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbfbc-112">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="fbfbc-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="fbfbc-113">**Chaîne** qui contient la restriction dont la valeur doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-113">A **String** that contains the restriction whose value is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbfbc-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fbfbc-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="fbfbc-115">JScript</span><span class="sxs-lookup"><span data-stu-id="fbfbc-115">JScript</span></span>

<span data-ttu-id="fbfbc-116">Type : **entier \***</span><span class="sxs-lookup"><span data-stu-id="fbfbc-116">Type: **Integer\***</span></span>

<span data-ttu-id="fbfbc-117">Valeur de la restriction.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-117">The value of the restriction.</span></span> <span data-ttu-id="fbfbc-118">Si la restriction spécifiée est introuvable, la valeur de retour est 0.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-118">If the specified restriction is not found, the return value is 0.</span></span>

### <a name="vb"></a><span data-ttu-id="fbfbc-119">VB</span><span class="sxs-lookup"><span data-stu-id="fbfbc-119">VB</span></span>

<span data-ttu-id="fbfbc-120">Type : **entier \***</span><span class="sxs-lookup"><span data-stu-id="fbfbc-120">Type: **Integer\***</span></span>

<span data-ttu-id="fbfbc-121">Valeur de la restriction.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-121">The value of the restriction.</span></span> <span data-ttu-id="fbfbc-122">Si la restriction spécifiée est introuvable, la valeur de retour est 0.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-122">If the specified restriction is not found, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbfbc-123">Notes </span><span class="sxs-lookup"><span data-stu-id="fbfbc-123">Remarks</span></span>

<span data-ttu-id="fbfbc-124">**IsRestricted** recherche d’abord un nom de sous-clé qui correspond à *sGroup* sous la clé suivante.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-124">**IsRestricted** first looks for a subkey name that matches *sGroup* under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

<span data-ttu-id="fbfbc-125">Les restrictions sont déclarées en tant que valeurs des sous-clés de stratégie individuelles.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-125">Restrictions are declared as values of the individual policy subkeys.</span></span> <span data-ttu-id="fbfbc-126">Si la restriction nommée dans *sRestriction* se trouve dans la sous-clé nommée dans *sGroup*, **IsRestricted** retourne la valeur actuelle de la restriction.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-126">If the restriction named in *sRestriction* is found in the subkey named in *sGroup*, **IsRestricted** returns the restriction's current value.</span></span> <span data-ttu-id="fbfbc-127">Si la restriction est introuvable sous **HKEY \_ local \_ machine**, la même sous-clé est vérifiée sous **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-127">If the restriction is not found under **HKEY\_LOCAL\_MACHINE**, the same subkey is checked under **HKEY\_CURRENT\_USER**.</span></span>

<span data-ttu-id="fbfbc-128">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-128">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="fbfbc-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="fbfbc-129">Examples</span></span>

<span data-ttu-id="fbfbc-130">Les exemples suivants illustrent l’utilisation de **IsRestricted** pour récupérer la valeur de données de la restriction **undockwithoutlogon** à partir de la sous-clé **système** .</span><span class="sxs-lookup"><span data-stu-id="fbfbc-130">The following examples show the use of **IsRestricted** to retrieve the data value of the **undockwithoutlogon** restriction from the **System** subkey.</span></span> <span data-ttu-id="fbfbc-131">L’utilisation est indiquée pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="fbfbc-131">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="fbfbc-132">Langage</span><span class="sxs-lookup"><span data-stu-id="fbfbc-132">JScript:</span></span>


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



<span data-ttu-id="fbfbc-133">VBScript</span><span class="sxs-lookup"><span data-stu-id="fbfbc-133">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="fbfbc-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbfbc-134">Requirements</span></span>



| <span data-ttu-id="fbfbc-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fbfbc-135">Requirement</span></span> | <span data-ttu-id="fbfbc-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbfbc-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbfbc-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbfbc-137">Minimum supported client</span></span><br/> | <span data-ttu-id="fbfbc-138">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbfbc-138">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fbfbc-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbfbc-139">Minimum supported server</span></span><br/> | <span data-ttu-id="fbfbc-140">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbfbc-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fbfbc-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="fbfbc-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbfbc-142"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbfbc-142"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="fbfbc-143">MIDL</span><span class="sxs-lookup"><span data-stu-id="fbfbc-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fbfbc-144"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fbfbc-144"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="fbfbc-145">DLL</span><span class="sxs-lookup"><span data-stu-id="fbfbc-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbfbc-146"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="fbfbc-146"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
