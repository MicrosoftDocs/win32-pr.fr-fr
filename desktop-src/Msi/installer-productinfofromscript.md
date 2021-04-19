---
description: La propriété ProductInfoFromScript de l’objet installer retourne la valeur de l’attribut spécifié qui est stocké dans un script de publication.
ms.assetid: 92aa479b-2b4c-482c-a186-a290461bc6d8
title: Programme d’installation ::P propriété roductInfoFromScript
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfoFromScript
- Installer.put_ProductInfoFromScript
- Installer.ProductInfoFromScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a4c8e29adb93f68228008770a95ad9fb9185e966
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530013"
---
# <a name="installerproductinfofromscript-property"></a><span data-ttu-id="48d78-103">Programme d’installation ::P propriété roductInfoFromScript</span><span class="sxs-lookup"><span data-stu-id="48d78-103">Installer::ProductInfoFromScript property</span></span>

<span data-ttu-id="48d78-104">La propriété **ProductInfoFromScript** de l’objet [**installer**](installer-object.md) retourne la valeur de l’attribut spécifié qui est stocké dans un script de publication.</span><span class="sxs-lookup"><span data-stu-id="48d78-104">The **ProductInfoFromScript** property of the [**Installer**](installer-object.md) object returns the value of the specified attribute that is stored in an advertise script.</span></span>

<span data-ttu-id="48d78-105">Cette propriété est en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="48d78-105">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="48d78-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="48d78-106">Syntax</span></span>


```JScript
Installer.ProductInfoFromScript = propVal 
```



## <a name="property-value"></a><span data-ttu-id="48d78-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="48d78-107">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="48d78-108">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="48d78-108">Error codes</span></span>

<span data-ttu-id="48d78-109">Valeur de chaîne ou d’entier en fonction de l’attribut demandé.</span><span class="sxs-lookup"><span data-stu-id="48d78-109">A string or integer value depending upon requested attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="48d78-110">Notes</span><span class="sxs-lookup"><span data-stu-id="48d78-110">Remarks</span></span>

<span data-ttu-id="48d78-111">La propriété **ProductInfoFromScript** utilise la fonction [**MsiGetProductInfoFromScript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) .</span><span class="sxs-lookup"><span data-stu-id="48d78-111">The **ProductInfoFromScript** property uses the [**MsiGetProductInfoFromScript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) function.</span></span>

## <a name="examples"></a><span data-ttu-id="48d78-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="48d78-112">Examples</span></span>

<span data-ttu-id="48d78-113">L’exemple de script suivant illustre l’utilisation de la propriété **ProductInfoFromScript** .</span><span class="sxs-lookup"><span data-stu-id="48d78-113">The following sample script demonstrates the use of the **ProductInfoFromScript** property .</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Create an advertise script for Orca
'

installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scratch\orca.aas"

' 
' Output ProductName Information From Script
'

MsgBox  installer.ProductInfoFromScript("c:\scratch\orca.aas", 3)
```



## <a name="requirements"></a><span data-ttu-id="48d78-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48d78-114">Requirements</span></span>



| <span data-ttu-id="48d78-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="48d78-115">Requirement</span></span> | <span data-ttu-id="48d78-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="48d78-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d78-117">Version</span><span class="sxs-lookup"><span data-stu-id="48d78-117">Version</span></span><br/> | <span data-ttu-id="48d78-118">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="48d78-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="48d78-119">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="48d78-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="48d78-120">Windows Installer 4,5 sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="48d78-120">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="48d78-121">DLL</span><span class="sxs-lookup"><span data-stu-id="48d78-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="48d78-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48d78-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="48d78-123">IID</span><span class="sxs-lookup"><span data-stu-id="48d78-123">IID</span></span><br/>     | <span data-ttu-id="48d78-124">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="48d78-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="48d78-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48d78-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48d78-126">**Programme d’installation**</span><span class="sxs-lookup"><span data-stu-id="48d78-126">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="48d78-127">Non pris en charge dans Windows Installer 3,1 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="48d78-127">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




