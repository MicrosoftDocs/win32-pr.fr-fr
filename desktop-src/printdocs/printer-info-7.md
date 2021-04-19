---
description: La \_ structure info 7 de l’imprimante \_ spécifie les informations d’imprimante des services d’annuaire.
ms.assetid: 9443855e-df7d-41a1-a0df-5649a97b2915
title: Structure PRINTER_INFO_7 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_7
- _PRINTER_INFO_7A
- _PRINTER_INFO_7W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3dfa92ead4a1f7dab4f0610145e1e1dee7d04065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541991"
---
# <a name="printer_info_7-structure"></a><span data-ttu-id="2b924-103">\_Structure info 7 de l’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="2b924-103">PRINTER\_INFO\_7 structure</span></span>

<span data-ttu-id="2b924-104">La **structure \_ info \_ 7** de l’imprimante spécifie les informations d’imprimante des services d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="2b924-104">The **PRINTER\_INFO\_7** structure specifies directory services printer information.</span></span> <span data-ttu-id="2b924-105">Utilisez cette structure avec la fonction [**SetPrinter**](setprinter.md) pour publier les données d’une imprimante dans le service d’annuaire (DS), ou pour mettre à jour ou supprimer les données publiées de l’imprimante à partir du DS.</span><span class="sxs-lookup"><span data-stu-id="2b924-105">Use this structure with the [**SetPrinter**](setprinter.md) function to publish a printer's data in the directory service (DS), or to update or remove a printer's published data from the DS.</span></span> <span data-ttu-id="2b924-106">Utilisez cette structure avec la fonction [**GetPrinter**](getprinter.md) pour déterminer si une imprimante est publiée dans le service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="2b924-106">Use this structure with the [**GetPrinter**](getprinter.md) function to determine whether a printer is published in the DS.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b924-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b924-107">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_7 {
  LPTSTR pszObjectGUID;
  DWORD  dwAction;
} PRINTER_INFO_7, *PPRINTER_INFO_7;
```



## <a name="members"></a><span data-ttu-id="2b924-108">Membres</span><span class="sxs-lookup"><span data-stu-id="2b924-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2b924-109">**pszObjectGUID**</span><span class="sxs-lookup"><span data-stu-id="2b924-109">**pszObjectGUID**</span></span>
</dt> <dd>

<span data-ttu-id="2b924-110">Pointeur vers une chaîne se terminant par un caractère null qui contient le GUID de l’objet de file d’attente à l’impression du service d’annuaire associé à une imprimante publiée.</span><span class="sxs-lookup"><span data-stu-id="2b924-110">A pointer to a null-terminated string containing the GUID of the directory service print queue object associated with a published printer.</span></span> <span data-ttu-id="2b924-111">Utilisez la fonction [**GetPrinter**](getprinter.md) pour récupérer ce GUID.</span><span class="sxs-lookup"><span data-stu-id="2b924-111">Use the [**GetPrinter**](getprinter.md) function to retrieve this GUID.</span></span>

<span data-ttu-id="2b924-112">Avant d’appeler [**SetPrinter**](setprinter.md), affectez la valeur **null** à **pszObjectGUID** .</span><span class="sxs-lookup"><span data-stu-id="2b924-112">Before calling [**SetPrinter**](setprinter.md), set **pszObjectGUID** to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2b924-113">**dwAction**</span><span class="sxs-lookup"><span data-stu-id="2b924-113">**dwAction**</span></span>
</dt> <dd>

<span data-ttu-id="2b924-114">Indique l’action à effectuer par la fonction [**SetPrinter**](setprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="2b924-114">Indicates the action for the [**SetPrinter**](setprinter.md) function to perform.</span></span> <span data-ttu-id="2b924-115">Pour la fonction [**GetPrinter**](getprinter.md) , ce membre indique si l’imprimante spécifiée est publiée.</span><span class="sxs-lookup"><span data-stu-id="2b924-115">For the [**GetPrinter**](getprinter.md) function, this member indicates whether the specified printer is published.</span></span> <span data-ttu-id="2b924-116">Ce membre peut être une combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2b924-116">This member can be a combination of the following values.</span></span>



| <span data-ttu-id="2b924-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b924-117">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="2b924-118">Signification</span><span class="sxs-lookup"><span data-stu-id="2b924-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DSPRINT_PENDING"></span><span id="dsprint_pending"></span><dl> <span data-ttu-id="2b924-119"><dt>**DSPRINT \_ 0x80000000 en attente**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2b924-119"><dt>**DSPRINT\_PENDING**</dt> <dt>0x80000000</dt></span></span> </dl>       | <span data-ttu-id="2b924-120">[**GetPrinter**](getprinter.md): indique que le système tente de terminer une opération de publication ou d’annulation de publication lancée par un appel [**SetPrinter**](setprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="2b924-120">[**GetPrinter**](getprinter.md): Indicates that the system is attempting to complete a publish or unpublish operation started by a [**SetPrinter**](setprinter.md) call.</span></span><br/> <span data-ttu-id="2b924-121">[**SetPrinter**](setprinter.md): cette valeur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2b924-121">[**SetPrinter**](setprinter.md): This value is not valid.</span></span> <br/>                                                |
| <span id="DSPRINT_PUBLISH"></span><span id="dsprint_publish"></span><dl> <span data-ttu-id="2b924-122"><dt>**DSPRINT \_ PUBLIER**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="2b924-122"><dt>**DSPRINT\_PUBLISH**</dt> <dt>0x00000001</dt></span></span> </dl>       | <span data-ttu-id="2b924-123">[**SetPrinter**](setprinter.md): publie les données de l’imprimante dans le service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="2b924-123">[**SetPrinter**](setprinter.md): Publishes the printer's data in the DS.</span></span><br/> <span data-ttu-id="2b924-124">[**GetPrinter**](getprinter.md): indique que l’imprimante est publiée.</span><span class="sxs-lookup"><span data-stu-id="2b924-124">[**GetPrinter**](getprinter.md): Indicates the printer is published.</span></span> <br/>                                                                                                                                      |
| <span id="DSPRINT_REPUBLISH"></span><span id="dsprint_republish"></span><dl> <span data-ttu-id="2b924-125"><dt>**DSPRINT \_ Republier**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="2b924-125"><dt>**DSPRINT\_REPUBLISH**</dt> <dt>0x00000008</dt></span></span> </dl> | <span data-ttu-id="2b924-126">[**SetPrinter**](setprinter.md): les données du service d’annuaire pour l’imprimante ne sont pas publiées, puis publiées à nouveau, ce qui a pour actualiser toutes les propriétés de l’imprimante publiée.</span><span class="sxs-lookup"><span data-stu-id="2b924-126">[**SetPrinter**](setprinter.md): The DS data for the printer is unpublished and then published again, refreshing all properties in the published printer.</span></span> <span data-ttu-id="2b924-127">La republication modifie également le GUID de l’imprimante publiée.</span><span class="sxs-lookup"><span data-stu-id="2b924-127">Re-publishing also changes the GUID of the published printer.</span></span><br/> <span data-ttu-id="2b924-128">[**GetPrinter**](getprinter.md): ne retourne jamais cette valeur.</span><span class="sxs-lookup"><span data-stu-id="2b924-128">[**GetPrinter**](getprinter.md): Never returns this value.</span></span> <br/> |
| <span id="DSPRINT_UNPUBLISH"></span><span id="dsprint_unpublish"></span><dl> <span data-ttu-id="2b924-129"><dt>**DSPRINT \_ Annuler la publication**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="2b924-129"><dt>**DSPRINT\_UNPUBLISH**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="2b924-130">[**SetPrinter**](setprinter.md): supprime les données publiées de l’imprimante du service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="2b924-130">[**SetPrinter**](setprinter.md): Removes the printer's published data from the DS.</span></span><br/> <span data-ttu-id="2b924-131">[**GetPrinter**](getprinter.md): indique que l’imprimante n’est pas publiée.</span><span class="sxs-lookup"><span data-stu-id="2b924-131">[**GetPrinter**](getprinter.md): Indicates the printer is not published.</span></span> <br/>                                                                                                                        |
| <span id="DSPRINT_UPDATE"></span><span id="dsprint_update"></span><dl> <span data-ttu-id="2b924-132"><dt>**DSPRINT \_ METTRE à jour**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="2b924-132"><dt>**DSPRINT\_UPDATE**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="2b924-133">[**SetPrinter**](setprinter.md): met à jour les données publiées de l’imprimante dans le service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="2b924-133">[**SetPrinter**](setprinter.md): Updates the printer's published data in the DS.</span></span><br/> <span data-ttu-id="2b924-134">[**GetPrinter**](getprinter.md): ne retourne jamais cette valeur.</span><span class="sxs-lookup"><span data-stu-id="2b924-134">[**GetPrinter**](getprinter.md): Never returns this value.</span></span> <br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b924-135">Notes</span><span class="sxs-lookup"><span data-stu-id="2b924-135">Remarks</span></span>

<span data-ttu-id="2b924-136">La **structure \_ info \_ 7** de l’imprimante est utilisée dans un appel [**SetPrinter**](setprinter.md) pour publier des informations sur l’imprimante dans le service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="2b924-136">The **PRINTER\_INFO\_7** structure is used in a [**SetPrinter**](setprinter.md) call to publish printer information to the directory service.</span></span> <span data-ttu-id="2b924-137">Les données publiées incluent l’ensemble des valeurs et des données pour l’imprimante spécifiée, qui se trouvent sous la \_ clé de spouleur SPLDS \_ , la clé de \_ pilote SPLDS ou les clés de clé d' \_ \_ utilisateur SPLDS \_ créées par [**SetPrinterDataEx**](setprinterdataex.md).</span><span class="sxs-lookup"><span data-stu-id="2b924-137">The published data includes all values and data for the specified printer found under the SPLDS\_SPOOLER\_KEY, SPLDS\_DRIVER\_KEY, or SPLDS\_USER\_KEY keys created by [**SetPrinterDataEx**](setprinterdataex.md).</span></span>

<span data-ttu-id="2b924-138">Pour [**SetPrinter**](setprinter.md), *pszObjectGUID* doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="2b924-138">For [**SetPrinter**](setprinter.md), *pszObjectGUID* should be set to **NULL**.</span></span> <span data-ttu-id="2b924-139">Pour [**GetPrinter**](getprinter.md), *PSZOBJECTGUID* retourne le GUID de l’objet file d’attente à l’impression des services d’annuaire associé à une imprimante publiée.</span><span class="sxs-lookup"><span data-stu-id="2b924-139">For [**GetPrinter**](getprinter.md), *pszObjectGUID* returns the GUID of the directory services print queue object associated with a published printer.</span></span> <span data-ttu-id="2b924-140">Vous pouvez utiliser ce GUID avec les méthodes de l’interface Active Directory Services (ADSI) pour récupérer les données publiées pour l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="2b924-140">You can use this GUID with Active Directory Services Interface (ADSI) methods to retrieve published data for the printer.</span></span> <span data-ttu-id="2b924-141">Toutefois, la méthode recommandée pour récupérer des données publiées consiste à appeler la fonction [**GetPrinterDataEx**](getprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="2b924-141">However, the recommended method for retrieving published data is to call the [**GetPrinterDataEx**](getprinterdataex.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b924-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b924-142">Requirements</span></span>



| <span data-ttu-id="2b924-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b924-143">Requirement</span></span> | <span data-ttu-id="2b924-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b924-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b924-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b924-145">Minimum supported client</span></span><br/> | <span data-ttu-id="2b924-146">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b924-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2b924-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b924-147">Minimum supported server</span></span><br/> | <span data-ttu-id="2b924-148">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b924-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2b924-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="2b924-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b924-150"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b924-150"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2b924-151">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="2b924-151">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2b924-152">**\_ \_ Infos sur \_ l’imprimante 7W** (Unicode) et **\_ \_ informations sur l’imprimante \_ 7A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2b924-152">**\_PRINTER\_INFO\_7W** (Unicode) and **\_PRINTER\_INFO\_7A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="2b924-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b924-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b924-154">Impression</span><span class="sxs-lookup"><span data-stu-id="2b924-154">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2b924-155">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="2b924-155">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




