---
description: Active la carte réseau.
ms.assetid: ceb71e1b-5107-420f-a677-814307340469
ms.tgt_platform: multiple
title: Activer la méthode de la classe Win32_NetworkAdapter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter.Enable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a7653d0bcda28ca333bc5c70bdcd69bce382787
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200953"
---
# <a name="enable-method-of-the-win32_networkadapter-class"></a><span data-ttu-id="2d47e-103">Activer la méthode de la \_ classe NetworkAdapter Win32</span><span class="sxs-lookup"><span data-stu-id="2d47e-103">Enable method of the Win32\_NetworkAdapter class</span></span>

<span data-ttu-id="2d47e-104">La méthode **Enable** active la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="2d47e-104">The **Enable** method enables the network adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d47e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d47e-105">Syntax</span></span>


```mof
uint32 Enable();
```



## <a name="parameters"></a><span data-ttu-id="2d47e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d47e-106">Parameters</span></span>

<span data-ttu-id="2d47e-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2d47e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2d47e-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d47e-108">Return value</span></span>

<span data-ttu-id="2d47e-109">Retourne zéro (0) pour indiquer la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="2d47e-109">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="2d47e-110">Tout autre nombre indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="2d47e-110">Any other number indicates an error.</span></span> <span data-ttu-id="2d47e-111">Pour les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2d47e-111">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="remarks"></a><span data-ttu-id="2d47e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="2d47e-112">Remarks</span></span>

<span data-ttu-id="2d47e-113">Vous pouvez rencontrer des difficultés lors de l’utilisation de cette méthode si votre application ne dispose pas de l’accès administrateur privilidges.</span><span class="sxs-lookup"><span data-stu-id="2d47e-113">You may experience difficulty using this method if your application does not administrator access privilidges.</span></span>

## <a name="examples"></a><span data-ttu-id="2d47e-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="2d47e-114">Examples</span></span>

<span data-ttu-id="2d47e-115">L’exemple de script Visual Basic suivant active la première carte réseau et affiche l’état de la propriété **Netactived** .</span><span class="sxs-lookup"><span data-stu-id="2d47e-115">The following Visual Basic Script example enables the first network adapter and shows the status of the **NetEnabled** property.</span></span> <span data-ttu-id="2d47e-116">Pour plus d’informations, consultez la page [**SWbemObjectSet. ItemIndex**](/windows/desktop/wmisdk/swbemobjectset-itemindex).</span><span class="sxs-lookup"><span data-stu-id="2d47e-116">For more information, see [**SWbemObjectSet.ItemIndex**](/windows/desktop/wmisdk/swbemobjectset-itemindex).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colAdapters = _
    objWMIService.Execquery_
        ("Select * from Win32_NetworkAdapter Where NetEnabled=False")
For Each Adapter in colAdapters
    WScript.Echo Adapter.DeviceId & "    " & Adapter.Name
Next
errReturn = colAdapters.ItemIndex(0).Enable()
If errReturn <> 0 Then
    WScript.Echo "Enable Network adapter failed for adapter= "_
        & colAdapters.ItemIndex(0).DeviceId
Else 
    WScript.Echo "Enable Network adapter succeeded for adapter= "_
        & colAdapters.ItemIndex(0).DeviceId 
End If 
WScript.Echo "NetEnabled= " & colAdapters.ItemIndex(0).NetEnabled
```



## <a name="requirements"></a><span data-ttu-id="2d47e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d47e-117">Requirements</span></span>



| <span data-ttu-id="2d47e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d47e-118">Requirement</span></span> | <span data-ttu-id="2d47e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d47e-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d47e-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d47e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2d47e-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d47e-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2d47e-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d47e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2d47e-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d47e-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2d47e-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2d47e-124">Namespace</span></span><br/>                | <span data-ttu-id="2d47e-125">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2d47e-125">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2d47e-126">MOF</span><span class="sxs-lookup"><span data-stu-id="2d47e-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d47e-127"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d47e-127"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d47e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2d47e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d47e-129"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d47e-129"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d47e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d47e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d47e-131">**\_NetworkAdapter Win32**</span><span class="sxs-lookup"><span data-stu-id="2d47e-131">**Win32\_NetworkAdapter**</span></span>](win32-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="2d47e-132">Tâches WMI : mise en réseau</span><span class="sxs-lookup"><span data-stu-id="2d47e-132">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="2d47e-133">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="2d47e-133">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

