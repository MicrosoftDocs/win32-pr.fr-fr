---
description: Récupère l’objet FolderItemVerb pour un élément spécifié dans la collection.
ms.assetid: 65871926-0920-4ad6-82da-7aba0a3c0fab
title: FolderItemVerbs. Item, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 013215af3f5005e68b396312d0ef13fa974d8a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973202"
---
# <a name="folderitemverbsitem-method"></a><span data-ttu-id="0867e-103">FolderItemVerbs. Item, méthode</span><span class="sxs-lookup"><span data-stu-id="0867e-103">FolderItemVerbs.Item method</span></span>

<span data-ttu-id="0867e-104">Récupère l’objet [**FolderItemVerb**](folderitemverb.md) pour un élément spécifié dans la collection.</span><span class="sxs-lookup"><span data-stu-id="0867e-104">Retrieves the [**FolderItemVerb**](folderitemverb.md) object for a specified item in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0867e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0867e-105">Syntax</span></span>


```JScript
retVal = FolderItemVerbs.Item(
  iIndex
)
```



## <a name="parameters"></a><span data-ttu-id="0867e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0867e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0867e-107">*iIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0867e-107">*iIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0867e-108">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="0867e-108">Type: **Variant**</span></span>

<span data-ttu-id="0867e-109">Index de base zéro de l'élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="0867e-109">The zero-based index of the item to retrieve.</span></span> <span data-ttu-id="0867e-110">Cette valeur doit être inférieure à la valeur de la propriété [**Count**](folderitemverbs-count.md) .</span><span class="sxs-lookup"><span data-stu-id="0867e-110">This value must be less than the value of the [**Count**](folderitemverbs-count.md) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0867e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0867e-111">Return value</span></span>

<span data-ttu-id="0867e-112">Type : **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="0867e-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="0867e-113">Objet qui reçoit l’objet [**FolderItemVerb**](folderitemverb.md) .</span><span class="sxs-lookup"><span data-stu-id="0867e-113">Object that receives the [**FolderItemVerb**](folderitemverb.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="0867e-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="0867e-114">Examples</span></span>

<span data-ttu-id="0867e-115">L’exemple suivant utilise **Item** pour récupérer les premiers verbes de la collection disponibles dans le dossier du panneau de configuration et affiche son nom.</span><span class="sxs-lookup"><span data-stu-id="0867e-115">The following example uses **Item** to retrieve the first verbs in the collection available to the Control Panel folder and displays its name.</span></span> <span data-ttu-id="0867e-116">L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0867e-116">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="0867e-117">Langage</span><span class="sxs-lookup"><span data-stu-id="0867e-117">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfCONTROLS = 3;
        
        objFolder2 = objShell.NameSpace(ssfCONTROLS);

        if (objFolder2 != null)
        {
            var objVerbs;
            objVerbs = objFolder2.Self.Verbs();
 
            if (objVerbs != null)
            {
                var objFolderItemVerb;
                objFolderItemVerb = objVerbs.Item(0);
 
                if (objFolderItemVerb != null)
                {
                    alert(objFolderItemVerb.Name);
                }
            }
        }
    }
</script>
```



<span data-ttu-id="0867e-118">VBScript</span><span class="sxs-lookup"><span data-stu-id="0867e-118">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemVerbsItemVB()
        dim objShell
        dim objFolder2
        dim ssfCONTROLS
        
        ssfCONTROLS = 3
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace(ssfCONTROLS)
        if (not objFolder2 is nothing) then
            dim objVerbs
            set objVerbs = objFolder2.Self.Verbs

            if (not objVerbs is nothing) then
                dim objFolderItemVerb
                set objFolderItemVerb = objVerbs.Item(0)

                if (not objFolderItemVerb is nothing) then
                    alert(objFolderItemVerb.Name)
                end if

                set objFolderItemVerb = nothing
            end if

            set objVerbs = nothing
        end if

        set objFolder2 = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="0867e-119">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="0867e-119">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemVerbsItemVB()
    Dim objShell    As Shell
    Dim objFolder2  As Folder2
    Dim ssfCONTROLS As Long
            
    ssfCONTROLS = 3
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfPROGRAMS)

    If (Not objFolder2 Is Nothing) Then
        Dim objVerbs As FolderItemVerbs
        Set objVerbs = objFolder2.Self.Verbs

        If (Not objVerbs Is Nothing) Then
            Dim objFolderItemVerb As FolderItemVerb
            Set objFolderItemVerb = objVerbs.Item(0)

            If (Not objFolderItemVerb Is Nothing) Then
                Debug.Print objFolderItemVerb.Name
            End If

            Set objFolderItemVerb = Nothing
        End If

        Set objVerbs = Nothing
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="0867e-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0867e-120">Requirements</span></span>



| <span data-ttu-id="0867e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0867e-121">Requirement</span></span> | <span data-ttu-id="0867e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="0867e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0867e-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0867e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0867e-124">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0867e-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0867e-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0867e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0867e-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0867e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0867e-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="0867e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0867e-128"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0867e-128"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="0867e-129">MIDL</span><span class="sxs-lookup"><span data-stu-id="0867e-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0867e-130"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0867e-130"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="0867e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0867e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0867e-132"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="0867e-132"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
