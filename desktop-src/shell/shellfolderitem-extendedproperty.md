---
description: Obtient la valeur d’une propriété à partir du jeu de propriétés d’un élément. La propriété peut être spécifiée par nom ou par l’identificateur de format (FMTID) et l’identificateur de propriété (PID) du jeu de propriétés.
ms.assetid: ca787d7b-d95a-45b9-9627-fd505f99f868
title: Méthode ShellFolderItem. ExtendedProperty (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.ExtendedProperty
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 614e42512b17a0d8a6950ac96914128b8746c685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973591"
---
# <a name="shellfolderitemextendedproperty-method"></a><span data-ttu-id="41219-104">Méthode ShellFolderItem. ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="41219-104">ShellFolderItem.ExtendedProperty method</span></span>

<span data-ttu-id="41219-105">Obtient la valeur d’une propriété à partir du jeu de propriétés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="41219-105">Gets the value of a property from an item's property set.</span></span> <span data-ttu-id="41219-106">La propriété peut être spécifiée par nom ou par l’identificateur de format (FMTID) et l’identificateur de propriété (PID) du jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="41219-106">The property can be specified either by name or by the property set's format identifier (FMTID) and property identifier (PID).</span></span>

## <a name="syntax"></a><span data-ttu-id="41219-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41219-107">Syntax</span></span>


```JScript
retVal = ShellFolderItem.ExtendedProperty(
  sPropName
)
```



## <a name="parameters"></a><span data-ttu-id="41219-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41219-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41219-109">*sPropName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="41219-109">*sPropName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41219-110">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="41219-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="41219-111">Valeur de **chaîne** qui spécifie la propriété.</span><span class="sxs-lookup"><span data-stu-id="41219-111">A **String** value that specifies the property.</span></span> <span data-ttu-id="41219-112">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="41219-112">See the Remarks section for details.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41219-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="41219-113">Return value</span></span>

<span data-ttu-id="41219-114">Type : \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="41219-114">Type: \**Variant\** _</span></span>

<span data-ttu-id="41219-115">Lorsque cette méthode est retournée, contient la valeur de la propriété, si elle existe pour l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="41219-115">When this method returns, contains the value of the property, if it exists for the specified item.</span></span> <span data-ttu-id="41219-116">La valeur aura un typage complet, par exemple, les dates sont retournées en tant que dates, et non en tant que chaînes.</span><span class="sxs-lookup"><span data-stu-id="41219-116">The value will have full typing—for example, dates are returned as dates, not strings.</span></span>

<span data-ttu-id="41219-117">Cette méthode retourne une chaîne de longueur nulle si la propriété est valide mais n’existe pas pour l’élément spécifié, ou un code d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="41219-117">This method returns a zero-length string if the property is valid but does not exist for the specified item, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="41219-118">Notes</span><span class="sxs-lookup"><span data-stu-id="41219-118">Remarks</span></span>

<span data-ttu-id="41219-119">Il existe deux façons de spécifier une propriété.</span><span class="sxs-lookup"><span data-stu-id="41219-119">There are two ways to specify a property.</span></span> <span data-ttu-id="41219-120">La première consiste à affecter le nom bien connu de la propriété, tel que « Author » ou « date », à _sPropName \*.</span><span class="sxs-lookup"><span data-stu-id="41219-120">The first is to assign the property's well-known name, such as "Author" or "Date", to _sPropName\*.</span></span> <span data-ttu-id="41219-121">Toutefois, chaque propriété est membre d’un jeu de propriétés COM (Component Object Model) et peut également être identifiée en spécifiant son ID de format (FMTID) et son ID de propriété (PID).</span><span class="sxs-lookup"><span data-stu-id="41219-121">However, each property is a member of a Component Object Model (COM) property set and can also be identified by specifying its format ID (FMTID) and property ID (PID).</span></span> <span data-ttu-id="41219-122">Un [**fmtid**](../stg/structured-storage-serialized-property-set-format.md) est un GUID qui identifie le jeu de propriétés, et un [**PID**](../stg/structured-storage-serialized-property-set-format.md) est un entier qui identifie une propriété particulière dans le jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="41219-122">An [**FMTID**](../stg/structured-storage-serialized-property-set-format.md) is a GUID that identifies the property set, and a [**PID**](../stg/structured-storage-serialized-property-set-format.md) is an integer that identifies a particular property within the property set.</span></span>

<span data-ttu-id="41219-123">La spécification d’une propriété par ses valeurs FMTID/PID est généralement plus efficace que l’utilisation de son nom.</span><span class="sxs-lookup"><span data-stu-id="41219-123">Specifying a property by its FMTID/PID values is usually more efficient than using its name.</span></span> <span data-ttu-id="41219-124">Pour utiliser les valeurs FMTID/PID d’une propriété avec **ExtendedProperty**, elles doivent être combinées dans un scid.</span><span class="sxs-lookup"><span data-stu-id="41219-124">To use a property's FMTID/PID values with **ExtendedProperty**, they must be combined into an SCID.</span></span> <span data-ttu-id="41219-125">Un SCID est une chaîne qui contient les valeurs FMTID/PID sous la forme «*fmtid \* \* PID*», où fmtid est le format de chaîne du GUID du jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="41219-125">An SCID is a string that contains the FMTID/PID values in the form "*FMTID\*\*PID*", where the FMTID is the string form of the property set's GUID.</span></span> <span data-ttu-id="41219-126">Par exemple, le SCID de la propriété auteur du jeu de propriétés des informations de résumé est « {F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4 ».</span><span class="sxs-lookup"><span data-stu-id="41219-126">For example, the SCID of the summary information property set's author property is "{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4".</span></span>

<span data-ttu-id="41219-127">Pour obtenir la liste des FMTIDs et des PID actuellement pris en charge par l’interpréteur de commandes, consultez [**SHCOLUMNID**](./objects.md).</span><span class="sxs-lookup"><span data-stu-id="41219-127">For a list of FMTIDs and PIDs that are currently supported by the Shell, see [**SHCOLUMNID**](./objects.md).</span></span>

## <a name="examples"></a><span data-ttu-id="41219-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="41219-128">Examples</span></span>

<span data-ttu-id="41219-129">Cet exemple de code illustre comment utiliser **ExtendedProperty** pour récupérer les propriétés « Title » et « Author » à partir d’un document Word.</span><span class="sxs-lookup"><span data-stu-id="41219-129">This sample code illustrates how to use **ExtendedProperty** to retrieve the "Title" and "Author" properties from a Word document.</span></span> <span data-ttu-id="41219-130">Une fois que vous avez l’objet [**ShellFolderItem**](shellfolderitem-object.md) associé au fichier, *fiWordDoc* dans cet exemple, récupérez la valeur de la propriété en passant son nom à **ExtendedProperty**.</span><span class="sxs-lookup"><span data-stu-id="41219-130">Once you have the [**ShellFolderItem**](shellfolderitem-object.md) object associated with the file, *fiWordDoc* in this example, retrieve the property's value by passing its name to **ExtendedProperty**.</span></span>


```none
...
Doc_Title=fiWordDoc.ExtendedProperty("DocTitle")
Doc_Author=fiWordDoc.ExtendedProperty("Author")
...
```



<span data-ttu-id="41219-131">Une approche plus rapide et plus efficace consiste à passer un SCID à **ExtendedProperty**.</span><span class="sxs-lookup"><span data-stu-id="41219-131">A faster and more efficient approach is to pass an SCID to **ExtendedProperty**.</span></span>


```none
...
FMTID_SummaryInfo="{F29F85E0-4FF9-1068-AB91-08002B27B3D9}"
PID_TITLE="2"
PID_AUTHOR="4"
SCID_TITLE=FMTID_SummaryInfo+" "+PID_TITLE
SCID_AUTHOR=FMTID_SummaryInfo+" "+PID_AUTHOR
Doc_Title=fiWordDoc.ExtendedProperty(SCID_TITLE)
Doc_Author=fiWordDoc.ExtendedProperty(SCID_AUTHOR)
...
```



<span data-ttu-id="41219-132">Les exemples suivants illustrent l’utilisation appropriée de cette méthode pour JScript, VBScript et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="41219-132">The following examples show the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="41219-133">Langage</span><span class="sxs-lookup"><span data-stu-id="41219-133">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItem2ExtendedPropertyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                var szReturn = "";
                
                szReturn = objFolderItem.ExtendedProperty("infotip");
                alert(szReturn);
            }
        }
    }
</script>
```



<span data-ttu-id="41219-134">VBScript</span><span class="sxs-lookup"><span data-stu-id="41219-134">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemExtendedPropertyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    dim szReturn
                    
                    szReturn = objFolderItem.ExtendedProperty("type")
                    alert(szReturn)
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="41219-135">Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="41219-135">Visual Basic:</span></span>


```VB
Private Sub fnFolderItem2ExtendedPropertyVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem2 As Object
            
            Set objFolderItem2 = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem2 Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem2.ExtendedProperty("size")
                    Debug.Print szReturn
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem2 = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="41219-136">Spécifications</span><span class="sxs-lookup"><span data-stu-id="41219-136">Requirements</span></span>



| <span data-ttu-id="41219-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41219-137">Requirement</span></span> | <span data-ttu-id="41219-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="41219-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41219-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41219-139">Minimum supported client</span></span><br/> | <span data-ttu-id="41219-140">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41219-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="41219-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41219-141">Minimum supported server</span></span><br/> | <span data-ttu-id="41219-142">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41219-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="41219-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="41219-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="41219-144"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="41219-144"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="41219-145">MIDL</span><span class="sxs-lookup"><span data-stu-id="41219-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41219-146"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="41219-146"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="41219-147">DLL</span><span class="sxs-lookup"><span data-stu-id="41219-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41219-148"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="41219-148"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
