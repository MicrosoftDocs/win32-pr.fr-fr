---
description: La méthode de transfert de l’objet Item transfère les données d’un appareil vers un fichier. Cette méthode s’applique uniquement aux éléments de type périphérique.
ms.assetid: ed9696da-bd94-4063-80c2-311a7a441b10
title: Item. Transfer, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Transfer
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: a476f9653b7deced48394af0ecaa0ea0c8ae51e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524073"
---
# <a name="itemtransfer-method"></a><span data-ttu-id="a228d-104">Item. Transfer, méthode</span><span class="sxs-lookup"><span data-stu-id="a228d-104">Item.Transfer method</span></span>

<span data-ttu-id="a228d-105">La méthode de **transfert** de l’objet [**Item**](-wia-item.md) transfère les données d’un appareil vers un fichier.</span><span class="sxs-lookup"><span data-stu-id="a228d-105">The **Transfer** method of the [**Item**](-wia-item.md) object transfers data from a device to a file.</span></span> <span data-ttu-id="a228d-106">Cette méthode s’applique uniquement aux éléments de type périphérique.</span><span class="sxs-lookup"><span data-stu-id="a228d-106">This method applies only to device type items.</span></span>

## <a name="syntax"></a><span data-ttu-id="a228d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a228d-107">Syntax</span></span>


```JScript
Item.Transfer(
  Filename,
  AsyncTransfer = VARIANT_BOOL
)
```



## <a name="parameters"></a><span data-ttu-id="a228d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a228d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a228d-109">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a228d-109">*Filename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a228d-110">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a228d-110">Type: **BSTR**</span></span>

<span data-ttu-id="a228d-111">Spécifie le nom du fichier dans lequel les données sont transférées.</span><span class="sxs-lookup"><span data-stu-id="a228d-111">Specifies the name of the file to which the data is transferred.</span></span>

</dd> <dt>

<span data-ttu-id="a228d-112">*AsyncTransfer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a228d-112">*AsyncTransfer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a228d-113">Type : **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="a228d-113">Type: **VARIANT\_BOOL**</span></span>

<span data-ttu-id="a228d-114">Valeur booléenne qui spécifie si le transfert doit être exécuté en tant qu’appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="a228d-114">A Boolean value that specifies whether the transfer should be run as an asynchronous call.</span></span>

<dt>



 <span data-ttu-id="a228d-115">(Variante \_ Boolean</span><span class="sxs-lookup"><span data-stu-id="a228d-115">(VARIANT\_BOOL)</span></span>


</dt> <dd>

<span data-ttu-id="a228d-116">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="a228d-116">Default.</span></span> <span data-ttu-id="a228d-117">Définissez cette valeur sur **true** si l’appel doit être asynchrone (consultez la **section Notes**).</span><span class="sxs-lookup"><span data-stu-id="a228d-117">Set this value to **true** if the call should be asynchronous (see **Remarks**).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a228d-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a228d-118">Return value</span></span>

<span data-ttu-id="a228d-119">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a228d-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a228d-120">Notes</span><span class="sxs-lookup"><span data-stu-id="a228d-120">Remarks</span></span>

<span data-ttu-id="a228d-121">Cette méthode s’applique uniquement aux éléments de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="a228d-121">This method applies only to file type items.</span></span> <span data-ttu-id="a228d-122">La méthode vérifie que l’élément prend en charge cette méthode avant de tenter d’effectuer le transfert de données.</span><span class="sxs-lookup"><span data-stu-id="a228d-122">The method checks that the item supports this method before it attempts to complete the data transfer.</span></span>

<span data-ttu-id="a228d-123">Utilisez « Clipboard » comme paramètre de *nom de fichier* pour transférer un élément dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="a228d-123">Use "clipboard" as the *Filename* parameter to transfer an item to the clipboard.</span></span>

<span data-ttu-id="a228d-124">Affectez la valeur **false** à *AsyncTransfer* pour les transferts au sein d’une application ou d’un script qui s’exécute dans un environnement qui termine un processus à la fin d’un script, tel que Windows Script Host (WSH).</span><span class="sxs-lookup"><span data-stu-id="a228d-124">Set the *AsyncTransfer* value to **false** for transfers within any application or script that runs in an environment that terminates a process at the end of a script, such as Windows Script Host (WSH).</span></span> <span data-ttu-id="a228d-125">Dans le cas contraire, le script peut se terminer et le processus se terminer avant la fin du transfert.</span><span class="sxs-lookup"><span data-stu-id="a228d-125">Otherwise, the script may end, and the process terminate, before the transfer completes.</span></span>

<span data-ttu-id="a228d-126">La méthode de **transfert** n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="a228d-126">The **Transfer** method has no return value.</span></span> <span data-ttu-id="a228d-127">Une fois le transfert terminé, cette méthode envoie un événement [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md) au script ou à l’application.</span><span class="sxs-lookup"><span data-stu-id="a228d-127">Upon completion of a transfer, this method sends an [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md) event to the script or application.</span></span>

## <a name="examples"></a><span data-ttu-id="a228d-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="a228d-128">Examples</span></span>

<span data-ttu-id="a228d-129">L’exemple suivant illustre l’utilisation de la méthode de **transfert** pour transférer des données à partir d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="a228d-129">The following example demonstrates the use of the **Transfer** method to transfer data from a device.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    For Each objItem In objSelectedItems
        objItem.Transfer("c:\Folder\Filename.bmp")
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="a228d-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a228d-130">Requirements</span></span>



| <span data-ttu-id="a228d-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a228d-131">Requirement</span></span> | <span data-ttu-id="a228d-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="a228d-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a228d-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a228d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a228d-134">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a228d-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a228d-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a228d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a228d-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a228d-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a228d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a228d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a228d-138"><dt>Wiascr.dll (version 4,90 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="a228d-138"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




