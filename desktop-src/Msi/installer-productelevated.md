---
description: La propriété ProductElevated de l’objet installer retourne la valeur true si le produit est managé ou false si le produit n’est pas géré.
ms.assetid: 8126f5a0-751f-46c3-9014-208e9c2db34c
title: Programme d’installation ::P propriété roductElevated
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductElevated
- Installer.get_ProductElevated
- Installer.ProductElevated
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 22591c20cbabfda2eb052e4746e87739b9681804
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537675"
---
# <a name="installerproductelevated-property"></a><span data-ttu-id="2fc18-103">Programme d’installation ::P propriété roductElevated</span><span class="sxs-lookup"><span data-stu-id="2fc18-103">Installer::ProductElevated property</span></span>

<span data-ttu-id="2fc18-104">La propriété **ProductElevated** de l’objet [**installer**](installer-object.md) retourne la valeur true si le produit est managé ou false si le produit n’est pas géré.</span><span class="sxs-lookup"><span data-stu-id="2fc18-104">The **ProductElevated** property of the [**Installer**](installer-object.md) object returns True if the product is managed or False if the product is not managed.</span></span>

<span data-ttu-id="2fc18-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2fc18-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fc18-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fc18-106">Syntax</span></span>


```JScript
propVal = Installer.ProductElevated
```



## <a name="property-value"></a><span data-ttu-id="2fc18-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2fc18-107">Property value</span></span>

<span data-ttu-id="2fc18-108">GUID du code du produit complet du produit.</span><span class="sxs-lookup"><span data-stu-id="2fc18-108">The full product code GUID of the product.</span></span> <span data-ttu-id="2fc18-109">Ce paramètre est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="2fc18-109">This parameter is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fc18-110">Notes</span><span class="sxs-lookup"><span data-stu-id="2fc18-110">Remarks</span></span>

<span data-ttu-id="2fc18-111">La propriété **ProductElevated** utilise la fonction [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) .</span><span class="sxs-lookup"><span data-stu-id="2fc18-111">The **ProductElevated** property uses the [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) function.</span></span> <span data-ttu-id="2fc18-112">Le retour de la propriété ne prend pas en compte la stratégie [AlwaysInstallElevated a](alwaysinstallelevated.md) .</span><span class="sxs-lookup"><span data-stu-id="2fc18-112">The return of the property does not take into account the [AlwaysInstallElevated](alwaysinstallelevated.md) policy.</span></span>

## <a name="examples"></a><span data-ttu-id="2fc18-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="2fc18-113">Examples</span></span>

<span data-ttu-id="2fc18-114">L’exemple de script suivant illustre l’utilisation de la propriété **ProductElevated** .</span><span class="sxs-lookup"><span data-stu-id="2fc18-114">The following sample script demonstrates the use of the **ProductElevated** property .</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Install Orca tool per-machine
'
installer.InstallProduct "\\products\public\orca\orca.msi", "ALLUSERS=1"

'
' Verify Orca is managed
'

Dim bManaged
bManaged = installer.ProductElevated("{85F4CBCB-9BBC-4B50-A7D8-E1106771498D}")

If bManaged Then
    MsgBox "Success - Product Is Managed"
Else
    MsgBox "Failure - Product Is Not Managed"
End If
```



## <a name="requirements"></a><span data-ttu-id="2fc18-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2fc18-115">Requirements</span></span>



| <span data-ttu-id="2fc18-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2fc18-116">Requirement</span></span> | <span data-ttu-id="2fc18-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fc18-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fc18-118">Version</span><span class="sxs-lookup"><span data-stu-id="2fc18-118">Version</span></span><br/> | <span data-ttu-id="2fc18-119">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2fc18-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2fc18-120">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2fc18-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2fc18-121">Windows Installer 4,5 sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="2fc18-121">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="2fc18-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2fc18-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="2fc18-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fc18-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="2fc18-124">IID</span><span class="sxs-lookup"><span data-stu-id="2fc18-124">IID</span></span><br/>     | <span data-ttu-id="2fc18-125">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2fc18-125">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="2fc18-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fc18-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fc18-127">**Programme d’installation**</span><span class="sxs-lookup"><span data-stu-id="2fc18-127">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="2fc18-128">Non pris en charge dans Windows Installer 3,1 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="2fc18-128">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




