---
description: Les constantes suivantes constituent l’ensemble des commandes d’appareil matériel WIA (Windows Image Acquisition) valides.
ms.assetid: f86a0944-2f2a-467e-a9e8-4cdecfc50175
title: Commandes de l’appareil WIA (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CMD_SYNCHRONIZE
- WIA_CMD_TAKE_PICTURE
- WIA_CMD_DELETE_ALL_ITEMS
- WIA_CMD_CHANGE_DOCUMENT
- WIA_CMD_UNLOAD_DOCUMENT
- WIA_CMD_START_FEEDER
- WIA_CMD_STOP_FEEDER
- WIA_CMD_PAUSE_FEEDER
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 6e9e732520a256519ebcb21da84eac7ca8d8b630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862666"
---
# <a name="wia-device-commands"></a><span data-ttu-id="af522-103">Commandes de l’appareil WIA</span><span class="sxs-lookup"><span data-stu-id="af522-103">WIA Device Commands</span></span>

<span data-ttu-id="af522-104">Les constantes suivantes constituent l’ensemble des commandes d’appareil matériel WIA (Windows Image Acquisition) valides.</span><span class="sxs-lookup"><span data-stu-id="af522-104">The following constants form the set of valid Windows Image Acquisition (WIA) hardware device commands.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="af522-105">Constante</span><span class="sxs-lookup"><span data-stu-id="af522-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="af522-106">Description</span><span class="sxs-lookup"><span data-stu-id="af522-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_SYNCHRONIZE"></span><span id="wia_cmd_synchronize"></span><dl> <span data-ttu-id="af522-107"><dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="af522-107"><dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="af522-108">Fait en sorte que le minipilote de l’appareil synchronise les éléments mis en cache avec le périphérique matériel.</span><span class="sxs-lookup"><span data-stu-id="af522-108">Causes the device's minidriver to synchronize cached items with the hardware device.</span></span> <span data-ttu-id="af522-109">Si l’appareil prend en charge la méthode <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>IWiaItem :: AnalyzeItem</strong></a> , l’émission de cette commande amène le minipilote à abandonner les résultats de l’analyse et à rétablir l’état initial de l’élément.</span><span class="sxs-lookup"><span data-stu-id="af522-109">If the device supports the <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>IWiaItem::AnalyzeItem</strong></a> method, issuing this command causes the minidriver to discard the analysis results and reset the item to its initial state.</span></span> <span data-ttu-id="af522-110">Tous les pilotes doivent prendre en charge cette commande.</span><span class="sxs-lookup"><span data-stu-id="af522-110">All drivers must support this command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_TAKE_PICTURE"></span><span id="wia_cmd_take_picture"></span><dl> <span data-ttu-id="af522-111"><dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="af522-111"><dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="af522-112">Provoque l’acquisition d’une image par un appareil WIA.</span><span class="sxs-lookup"><span data-stu-id="af522-112">Causes a WIA device to acquire an image.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_DELETE_ALL_ITEMS"></span><span id="wia_cmd_delete_all_items"></span><dl> <span data-ttu-id="af522-113"><dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="af522-113"><dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="af522-114">Indique à l’appareil de supprimer tous les éléments qui peuvent être supprimés de l’arborescence des objets <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> qui représentent l’appareil.</span><span class="sxs-lookup"><span data-stu-id="af522-114">Tells the device to delete all items that can be deleted from the tree of <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> objects that represent the device.</span></span> <span data-ttu-id="af522-115">La suppression d’éléments est empêchée en définissant les propriétés de l’élément.</span><span class="sxs-lookup"><span data-stu-id="af522-115">Item deletion is prevented by setting the item's properties.</span></span> <span data-ttu-id="af522-116">Pour plus d’informations, consultez <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>IWiaPropertyStorage :: SetPropertyStream</strong></a> et <a href="-wia-property-attributes.md">attributs de propriété</a>.</span><span class="sxs-lookup"><span data-stu-id="af522-116">For details, see <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>IWiaPropertyStorage::SetPropertyStream</strong></a> and <a href="-wia-property-attributes.md">Property Attributes</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_CHANGE_DOCUMENT"></span><span id="wia_cmd_change_document"></span><dl> <span data-ttu-id="af522-117"><dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="af522-117"><dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="af522-118">Utilisé pour les scanneurs de documents.</span><span class="sxs-lookup"><span data-stu-id="af522-118">Used for document scanners.</span></span> <span data-ttu-id="af522-119">Fait en sorte que le scanneur charge la page suivante dans son gestionnaire de documents.</span><span class="sxs-lookup"><span data-stu-id="af522-119">Causes the scanner to load the next page in its document handler.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_UNLOAD_DOCUMENT"></span><span id="wia_cmd_unload_document"></span><dl> <span data-ttu-id="af522-120"><dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="af522-120"><dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="af522-121">Utilisé pour les scanneurs de documents.</span><span class="sxs-lookup"><span data-stu-id="af522-121">Used for document scanners.</span></span> <span data-ttu-id="af522-122">Indique à l’appareil de décharger toutes les pages restantes dans son gestionnaire de documents.</span><span class="sxs-lookup"><span data-stu-id="af522-122">Tells the device to unload all remaining pages in its document handler.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_START_FEEDER"></span><span id="wia_cmd_start_feeder"></span><dl> <span data-ttu-id="af522-123"><dt><strong>WIA_CMD_START_FEEDER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="af522-123"><dt><strong>WIA_CMD_START_FEEDER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="af522-124">Utilisé pour les scanneurs de documents qui ont un flux de page.</span><span class="sxs-lookup"><span data-stu-id="af522-124">Used for document scanners that have a page feeder.</span></span> <span data-ttu-id="af522-125">Indique à l’appareil de démarrer le moteur du chargeur.</span><span class="sxs-lookup"><span data-stu-id="af522-125">Tells the device to start the feeder motor.</span></span> <span data-ttu-id="af522-126">Cette fonctionnalité est disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="af522-126">This feature is available starting with Windows 8.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="af522-127">Le minipilote WIA doit rejeter cette commande et retourner <strong>WIA_ERROR_INVALID_COMMAND</strong> lorsque la propriété <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> n’est pas prise en charge ou est définie sur WIA_FEEDER_CONTROL_AUTO.</span><span class="sxs-lookup"><span data-stu-id="af522-127">The WIA minidriver must reject this command and return <strong>WIA_ERROR_INVALID_COMMAND</strong> when the <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> property is not supported, or is set to WIA_FEEDER_CONTROL_AUTO.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_STOP_FEEDER"></span><span id="wia_cmd_stop_feeder"></span><dl> <span data-ttu-id="af522-128"><dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="af522-128"><dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="af522-129">Utilisé pour les scanneurs de documents qui ont un flux de page.</span><span class="sxs-lookup"><span data-stu-id="af522-129">Used for document scanners that have a page feeder.</span></span> <span data-ttu-id="af522-130">Indique à l’appareil d’arrêter le moteur du chargeur.</span><span class="sxs-lookup"><span data-stu-id="af522-130">Tells the device to stop the feeder motor.</span></span> <span data-ttu-id="af522-131">Cette fonctionnalité est disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="af522-131">This feature is available starting with Windows 8.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="af522-132">Le minipilote WIA doit rejeter cette commande et retourner <strong>WIA_ERROR_INVALID_COMMAND</strong> lorsque la propriété <strong>WIA_IPS_FEEDER_CONTROL</strong> n’est pas prise en charge ou est définie sur WIA_FEEDER_CONTROL_AUTO.</span><span class="sxs-lookup"><span data-stu-id="af522-132">The WIA minidriver must reject this command and return <strong>WIA_ERROR_INVALID_COMMAND</strong> when the <strong>WIA_IPS_FEEDER_CONTROL</strong> property is not supported, or is set to WIA_FEEDER_CONTROL_AUTO.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_PAUSE_FEEDER"></span><span id="wia_cmd_pause_feeder"></span><dl> <span data-ttu-id="af522-133"><dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="af522-133"><dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="af522-134">Utilisé pour les scanneurs de documents qui ont un flux de page.</span><span class="sxs-lookup"><span data-stu-id="af522-134">Used for document scanners that have a page feeder.</span></span> <span data-ttu-id="af522-135">Indique à l’appareil d’interrompre le moteur du chargeur.</span><span class="sxs-lookup"><span data-stu-id="af522-135">Tells the device to pause the feeder motor.</span></span> <span data-ttu-id="af522-136">Cette fonctionnalité est disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="af522-136">This feature is available starting with Windows 8.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="af522-137">Le minipilote WIA doit rejeter cette commande et retourner <strong>WIA_ERROR_INVALID_COMMAND</strong> lorsque la propriété <strong>WIA_IPS_FEEDER_CONTROL</strong> n’est pas prise en charge ou est définie sur WIA_FEEDER_CONTROL_AUTO.</span><span class="sxs-lookup"><span data-stu-id="af522-137">The WIA minidriver must reject this command and return <strong>WIA_ERROR_INVALID_COMMAND</strong> when the <strong>WIA_IPS_FEEDER_CONTROL</strong> property is not supported, or is set to WIA_FEEDER_CONTROL_AUTO.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="af522-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af522-138">Requirements</span></span>



| <span data-ttu-id="af522-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af522-139">Requirement</span></span> | <span data-ttu-id="af522-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="af522-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="af522-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af522-141">Minimum supported client</span></span><br/> | <span data-ttu-id="af522-142">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af522-142">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="af522-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af522-143">Minimum supported server</span></span><br/> | <span data-ttu-id="af522-144">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af522-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="af522-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="af522-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="af522-146"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="af522-146"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
