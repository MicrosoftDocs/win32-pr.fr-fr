---
title: Méthodes de propriété IADsPrintQueueOperations (IADs. h)
description: Les méthodes de propriété de l’interface IADsPrintQueueOperations lisent et écrivent les propriétés répertoriées dans la liste suivante. Pour plus d’informations sur les méthodes de propriété, consultez Méthodes de propriété d’interface.
ms.assetid: a4e6bac5-5d52-4492-b48e-f051fec6158c
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsPrintQueueOperations ADSI
topic_type:
- apiref
api_name:
- IADsPrintQueueOperations Property Methods
- IADsPrintQueueOperations.Status
- IADsPrintQueueOperations.get_Name
- IADsPrintQueueOperations.put_Name
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8af7aef94dd9453af690f0c5d83b1e978d3b058
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942564"
---
# <a name="iadsprintqueueoperations-property-methods"></a><span data-ttu-id="9917d-105">Méthodes de propriété IADsPrintQueueOperations</span><span class="sxs-lookup"><span data-stu-id="9917d-105">IADsPrintQueueOperations Property Methods</span></span>

<span data-ttu-id="9917d-106">Les méthodes de propriété de l’interface [**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations) lisent et écrivent les propriétés répertoriées dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="9917d-106">The property methods of the [**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations) interface read and write the properties listed in the following list.</span></span> <span data-ttu-id="9917d-107">Pour plus d’informations sur les méthodes de propriété, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="9917d-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="9917d-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9917d-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="9917d-109">**État**</span><span class="sxs-lookup"><span data-stu-id="9917d-109">**Status**</span></span>
<span data-ttu-id="9917d-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9917d-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="9917d-111">État actuel des opérations de file d’attente à l’impression.</span><span class="sxs-lookup"><span data-stu-id="9917d-111">Current status of the print queue operations.</span></span> <span data-ttu-id="9917d-112">Les valeurs de code d’état valides sont répertoriées dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="9917d-112">The valid status code values are listed in the following list.</span></span>

<dt>

<span id="ADS_PRINTER_PAUSED"></span><span id="ads_printer_paused"></span>

<span data-ttu-id="9917d-113">**Annonces \_ IMPRIMANTE \_ suspendue** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="9917d-113">**ADS\_PRINTER\_PAUSED** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PENDING_DELETION"></span><span id="ads_printer_pending_deletion"></span>

<span data-ttu-id="9917d-114">**Annonces \_ IMPRIMANTE \_ en attente de \_ suppression** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="9917d-114">**ADS\_PRINTER\_PENDING\_DELETION** (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_ERROR"></span><span id="ads_printer_error"></span>

<span data-ttu-id="9917d-115">**Annonces \_ \_Erreur d’imprimante** (0x00000003)</span><span class="sxs-lookup"><span data-stu-id="9917d-115">**ADS\_PRINTER\_ERROR** (0x00000003)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_JAM"></span><span id="ads_printer_paper_jam"></span>

<span data-ttu-id="9917d-116">**Annonces \_ \_ \_ Bourrage papier** sur l’imprimante (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="9917d-116">**ADS\_PRINTER\_PAPER\_JAM** (0x00000004)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_OUT"></span><span id="ads_printer_paper_out"></span>

<span data-ttu-id="9917d-117">**Annonces \_ \_ \_ Sortie papier** de l’imprimante (0x00000005)</span><span class="sxs-lookup"><span data-stu-id="9917d-117">**ADS\_PRINTER\_PAPER\_OUT** (0x00000005)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_MANUAL_FEED"></span><span id="ads_printer_manual_feed"></span>

<span data-ttu-id="9917d-118">**Annonces \_ \_ \_ Alimentation manuelle** de l’imprimante (0x00000006)</span><span class="sxs-lookup"><span data-stu-id="9917d-118">**ADS\_PRINTER\_MANUAL\_FEED** (0x00000006)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_PROBLEM"></span><span id="ads_printer_paper_problem"></span>

<span data-ttu-id="9917d-119">**Annonces \_ \_ \_ Problème papier** sur l’imprimante (0x00000007)</span><span class="sxs-lookup"><span data-stu-id="9917d-119">**ADS\_PRINTER\_PAPER\_PROBLEM** (0x00000007)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OFFLINE"></span><span id="ads_printer_offline"></span>

<span data-ttu-id="9917d-120">**Annonces \_ IMPRIMANTE \_ hors connexion** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="9917d-120">**ADS\_PRINTER\_OFFLINE** (0x00000008)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_IO_ACTIVE"></span><span id="ads_printer_io_active"></span>

<span data-ttu-id="9917d-121">**Annonces \_ \_E/ \_ s d’imprimante active** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="9917d-121">**ADS\_PRINTER\_IO\_ACTIVE** (0x00000100)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_BUSY"></span><span id="ads_printer_busy"></span>

<span data-ttu-id="9917d-122">**Annonces \_ IMPRIMANTE \_ occupée** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="9917d-122">**ADS\_PRINTER\_BUSY** (0x00000200)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PRINTING"></span><span id="ads_printer_printing"></span>

<span data-ttu-id="9917d-123">**Annonces \_ \_Impression d’imprimante** (0x00000400)</span><span class="sxs-lookup"><span data-stu-id="9917d-123">**ADS\_PRINTER\_PRINTING** (0x00000400)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUTPUT_BIN_FULL"></span><span id="ads_printer_output_bin_full"></span>

<span data-ttu-id="9917d-124">**Annonces \_ Bac de sortie d’imprimante \_ \_ \_ plein** (0x00000800)</span><span class="sxs-lookup"><span data-stu-id="9917d-124">**ADS\_PRINTER\_OUTPUT\_BIN\_FULL** (0x00000800)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NOT_AVAILABLE"></span><span id="ads_printer_not_available"></span>

<span data-ttu-id="9917d-125">**Annonces \_ IMPRIMANTE \_ non \_ disponible** (0x00001000)</span><span class="sxs-lookup"><span data-stu-id="9917d-125">**ADS\_PRINTER\_NOT\_AVAILABLE** (0x00001000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WAITING"></span><span id="ads_printer_waiting"></span>

<span data-ttu-id="9917d-126">**Annonces \_ IMPRIMANTE en \_ attente** (0x00002000)</span><span class="sxs-lookup"><span data-stu-id="9917d-126">**ADS\_PRINTER\_WAITING** (0x00002000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PROCESSING"></span><span id="ads_printer_processing"></span>

<span data-ttu-id="9917d-127">**Annonces \_ \_Traitement** de l’imprimante (0x00004000)</span><span class="sxs-lookup"><span data-stu-id="9917d-127">**ADS\_PRINTER\_PROCESSING** (0x00004000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_INITIALIZING"></span><span id="ads_printer_initializing"></span>

<span data-ttu-id="9917d-128">**Annonces \_ \_Initialisation d’imprimante** (0x00008000)</span><span class="sxs-lookup"><span data-stu-id="9917d-128">**ADS\_PRINTER\_INITIALIZING** (0x00008000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WARMING_UP"></span><span id="ads_printer_warming_up"></span>

<span data-ttu-id="9917d-129">**Annonces \_ \_Préchauffage \_** de l’imprimante (0x00010000)</span><span class="sxs-lookup"><span data-stu-id="9917d-129">**ADS\_PRINTER\_WARMING\_UP** (0x00010000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_TONER_LOW"></span><span id="ads_printer_toner_low"></span>

<span data-ttu-id="9917d-130">**Annonces \_ \_Toner \_ faible** de l’imprimante (0x00020000)</span><span class="sxs-lookup"><span data-stu-id="9917d-130">**ADS\_PRINTER\_TONER\_LOW** (0x00020000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NO_TONER"></span><span id="ads_printer_no_toner"></span>

<span data-ttu-id="9917d-131">**Annonces \_ IMPRIMANTE \_ sans \_ toner** (0x00040000)</span><span class="sxs-lookup"><span data-stu-id="9917d-131">**ADS\_PRINTER\_NO\_TONER** (0x00040000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAGE_PUNT"></span><span id="ads_printer_page_punt"></span>

<span data-ttu-id="9917d-132">**Annonces \_ Page d’impression \_ \_ chargeur** (0x00080000)</span><span class="sxs-lookup"><span data-stu-id="9917d-132">**ADS\_PRINTER\_PAGE\_PUNT** (0x00080000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_USER_INTERVENTION"></span><span id="ads_printer_user_intervention"></span>

<span data-ttu-id="9917d-133">**Annonces \_ \_ \_ Intervention** de l’utilisateur de l’imprimante (0x00100000)</span><span class="sxs-lookup"><span data-stu-id="9917d-133">**ADS\_PRINTER\_USER\_INTERVENTION** (0x00100000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUT_OF_MEMORY"></span><span id="ads_printer_out_of_memory"></span>

<span data-ttu-id="9917d-134">**Annonces \_ \_ \_ \_ Mémoire insuffisante de l’imprimante** (0x00200000)</span><span class="sxs-lookup"><span data-stu-id="9917d-134">**ADS\_PRINTER\_OUT\_OF\_MEMORY** (0x00200000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_DOOR_OPEN"></span><span id="ads_printer_door_open"></span>

<span data-ttu-id="9917d-135">**Annonces \_ Capot de l’imprimante \_ \_ ouvert** (0x00400000)</span><span class="sxs-lookup"><span data-stu-id="9917d-135">**ADS\_PRINTER\_DOOR\_OPEN** (0x00400000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_SERVER_UNKNOWN"></span><span id="ads_printer_server_unknown"></span>

<span data-ttu-id="9917d-136">**Annonces \_ Serveur d’impression \_ \_ inconnu** (0x00800000)</span><span class="sxs-lookup"><span data-stu-id="9917d-136">**ADS\_PRINTER\_SERVER\_UNKNOWN** (0x00800000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_POWER_SAVE"></span><span id="ads_printer_power_save"></span>

<span data-ttu-id="9917d-137">**Annonces \_ Économie \_ d' \_ énergie d’imprimante** (0x01000000)</span><span class="sxs-lookup"><span data-stu-id="9917d-137">**ADS\_PRINTER\_POWER\_SAVE** (0x01000000)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="9917d-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="9917d-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9917d-139">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="9917d-139">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] LONG* pbstrName
);
HRESULT put_Name(
  [in] LONG bstrName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="9917d-140">Exemples</span><span class="sxs-lookup"><span data-stu-id="9917d-140">Examples</span></span>

<span data-ttu-id="9917d-141">L’exemple de code Visual Basic suivant vérifie qu’une imprimante est coincée.</span><span class="sxs-lookup"><span data-stu-id="9917d-141">The following Visual Basic code example verifies that a printer is jammed.</span></span>


```VB
Dim pqo As IADsPrintQueueOperations
Set pqo = GetObject("WinNT://aMachine/aPrinter")
If pqo.Status = ADS_PRINTER_PAPER_JAM Then
MsgBox "Your printer is jammed."
End If
```



<span data-ttu-id="9917d-142">L’exemple de code C++ suivant vérifie qu’une imprimante est coincée.</span><span class="sxs-lookup"><span data-stu-id="9917d-142">The following C++ code example verifies that a printer is jammed.</span></span>


```C++
IADsPrintQueueOperations *pqo;
HRESULT hr = ADsGetObject(L"WinNT://aMachine/aPrinter",
IID_IADsPrintQueueOperations,
(void**)&pqo)
long status;
hr = pqo->get_Status(&status);
if(status = ADS_PRINTER_PAPER_JAM) {
printf("Your printer is jammed.\n");
}
hr = pqo->Release();
```



## <a name="requirements"></a><span data-ttu-id="9917d-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9917d-143">Requirements</span></span>



| <span data-ttu-id="9917d-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9917d-144">Requirement</span></span> | <span data-ttu-id="9917d-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="9917d-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9917d-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9917d-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9917d-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9917d-147">Windows Vista</span></span><br/>                                                                    |
| <span data-ttu-id="9917d-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9917d-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9917d-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9917d-149">Windows Server 2008</span></span><br/>                                                              |
| <span data-ttu-id="9917d-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="9917d-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="9917d-151"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="9917d-151"><dt>Iads.h</dt></span></span> </dl>           |
| <span data-ttu-id="9917d-152">DLL</span><span class="sxs-lookup"><span data-stu-id="9917d-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9917d-153"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9917d-153"><dt>Activeds.dll</dt></span></span> </dl>     |
| <span data-ttu-id="9917d-154">IID</span><span class="sxs-lookup"><span data-stu-id="9917d-154">IID</span></span><br/>                      | <span data-ttu-id="9917d-155">IID \_ IADsPrintQueueOperations est défini en tant que 124BE5C0-156e-11CF-A986-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="9917d-155">IID\_IADsPrintQueueOperations is defined as 124BE5C0-156E-11CF-A986-00AA006BC149</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9917d-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9917d-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9917d-157">**IADsPrintQueue**</span><span class="sxs-lookup"><span data-stu-id="9917d-157">**IADsPrintQueue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[<span data-ttu-id="9917d-158">**IADsPrintQueueOperations**</span><span class="sxs-lookup"><span data-stu-id="9917d-158">**IADsPrintQueueOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)
</dt> </dl>

 

 





