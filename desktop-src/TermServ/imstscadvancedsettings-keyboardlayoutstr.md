---
title: IMsTscAdvancedSettings propriété KeyBoardLayoutStr
description: Spécifie le nom de l’identificateur de paramètres régionaux d’entrée actif (anciennement appelé disposition de clavier) à utiliser pour la connexion.
ms.assetid: a469c602-84a8-44c6-9c0f-76262961b527
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété KeyBoardLayoutStr
- Services Bureau à distance de la propriété KeyBoardLayoutStr, interface IMsTscAdvancedSettings
- Services Bureau à distance de l’interface IMsTscAdvancedSettings, propriété KeyBoardLayoutStr
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.KeyBoardLayoutStr
- IMsTscAdvancedSettings.put_KeyBoardLayoutStr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4d5e6703b86f5e60a50ead05f8015df61cfdc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741501"
---
# <a name="imstscadvancedsettingskeyboardlayoutstr-property"></a><span data-ttu-id="43a3f-106">IMsTscAdvancedSettings :: KeyBoardLayoutStr, propriété</span><span class="sxs-lookup"><span data-stu-id="43a3f-106">IMsTscAdvancedSettings::KeyBoardLayoutStr property</span></span>

<span data-ttu-id="43a3f-107">Spécifie le nom de l’identificateur de paramètres régionaux d’entrée actif (anciennement appelé disposition de clavier) à utiliser pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="43a3f-107">Specifies the name of the active input locale identifier (formerly called the keyboard layout) to use for the connection.</span></span>

<span data-ttu-id="43a3f-108">Si cette propriété n’est pas définie, le contrôle utilise la disposition par défaut retournée par la fonction [**GetKeyboardLayout**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout) .</span><span class="sxs-lookup"><span data-stu-id="43a3f-108">If this property is not set, the control uses the default layout returned by the [**GetKeyboardLayout**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout) function.</span></span>

<span data-ttu-id="43a3f-109">Cette propriété est en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="43a3f-109">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="43a3f-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43a3f-110">Syntax</span></span>


```C++
HRESULT put_KeyBoardLayoutStr(
  [in] BSTR KeyBoardLayoutStr
);
```



## <a name="property-value"></a><span data-ttu-id="43a3f-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="43a3f-111">Property value</span></span>

<span data-ttu-id="43a3f-112">Nom de l’identificateur de paramètres régionaux d’entrée actif.</span><span class="sxs-lookup"><span data-stu-id="43a3f-112">The name of the active input locale identifier.</span></span>

## <a name="error-codes"></a><span data-ttu-id="43a3f-113">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="43a3f-113">Error codes</span></span>

<span data-ttu-id="43a3f-114">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="43a3f-114">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="43a3f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="43a3f-115">Remarks</span></span>

<span data-ttu-id="43a3f-116">La propriété est un nombre hexadécimal à huit chiffres sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="43a3f-116">The property is an eight digit hexadecimal number in string form.</span></span> <span data-ttu-id="43a3f-117">Les quatre chiffres inférieurs représentent l’identificateur de langue, et les quatre chiffres supérieurs représentent la variation du clavier dans cette langue.</span><span class="sxs-lookup"><span data-stu-id="43a3f-117">The lower four digits represent the language identifier, and the upper four digits represent the keyboard variation within that language.</span></span> <span data-ttu-id="43a3f-118">Ainsi, par exemple, « 00000409 » représente le clavier anglais américain par défaut, car « 0409 » est l’identificateur de langue Anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="43a3f-118">So, for example, "00000409" would represent the default US English keyboard because "0409" is the US English language identifier.</span></span> <span data-ttu-id="43a3f-119">La variation Dvorak du clavier anglais des États-Unis a pour identificateur « 00010409 ».</span><span class="sxs-lookup"><span data-stu-id="43a3f-119">The Dvorak variation of the US English keyboard has an identifier of "00010409".</span></span> <span data-ttu-id="43a3f-120">Vous pouvez trouver les dispositions de clavier disponibles, listées par leurs identificateurs de disposition de clavier, dans le Registre sous</span><span class="sxs-lookup"><span data-stu-id="43a3f-120">You can find the available keyboard layouts, listed by their keyboard layout identifiers, in the registry under</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      ControlSet001
         Control
            Keyboard Layouts
```

<span data-ttu-id="43a3f-121">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="43a3f-121">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="43a3f-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43a3f-122">Requirements</span></span>



| <span data-ttu-id="43a3f-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43a3f-123">Requirement</span></span> | <span data-ttu-id="43a3f-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="43a3f-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="43a3f-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43a3f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="43a3f-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43a3f-126">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="43a3f-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43a3f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="43a3f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43a3f-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="43a3f-129">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="43a3f-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="43a3f-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43a3f-130"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="43a3f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="43a3f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43a3f-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43a3f-132"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="43a3f-133">IID</span><span class="sxs-lookup"><span data-stu-id="43a3f-133">IID</span></span><br/>                      | <span data-ttu-id="43a3f-134">IID \_ IMsTscAdvancedSettings est défini en tant que 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="43a3f-134">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43a3f-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43a3f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43a3f-136">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="43a3f-136">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

