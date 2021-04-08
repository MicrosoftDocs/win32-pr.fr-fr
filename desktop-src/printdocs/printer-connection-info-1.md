---
description: Représente des informations sur une connexion à une imprimante.
ms.assetid: afac3f91-74eb-46f7-94b4-d37b2b8a32a4
title: Structure PRINTER_CONNECTION_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_CONNECTION_INFO_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 04bfb5411a5602248bcd188d07dec8478462fd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757383"
---
# <a name="printer_connection_info_1-structure"></a><span data-ttu-id="df66a-103">Structure d’informations de connexion d’imprimante \_ \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="df66a-103">PRINTER\_CONNECTION\_INFO\_1 structure</span></span>

<span data-ttu-id="df66a-104">Représente des informations sur une connexion à une imprimante.</span><span class="sxs-lookup"><span data-stu-id="df66a-104">Represents information about a connection to a printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="df66a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df66a-105">Syntax</span></span>


```C++
typedef struct _PRINTER_CONNECTION_INFO_1 {
  DWORD  dwFlags;
  LPTSTR pszDriverName;
} PRINTER_CONNECTION_INFO_1, *PPRINTER_CONNECTION_INFO_1;
```



## <a name="members"></a><span data-ttu-id="df66a-106">Membres</span><span class="sxs-lookup"><span data-stu-id="df66a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="df66a-107">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="df66a-107">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="df66a-108">Les valeurs suivantes sont définies :</span><span class="sxs-lookup"><span data-stu-id="df66a-108">The following values are defined:</span></span>



| <span data-ttu-id="df66a-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="df66a-109">Value</span></span>                                      | <span data-ttu-id="df66a-110">Signification</span><span class="sxs-lookup"><span data-stu-id="df66a-110">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df66a-111">Non-concordance de la connexion à l’imprimante \_ \_ (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="df66a-111">PRINTER\_CONNECTION\_MISMATCH (0x00000020)</span></span> | <span data-ttu-id="df66a-112">Si cet indicateur de bit est défini, la connexion à l’imprimante n’est pas compatible.</span><span class="sxs-lookup"><span data-stu-id="df66a-112">If this bit-flag is set, the printer connection is mismatched.</span></span> <span data-ttu-id="df66a-113">L’utilisateur peut fournir un pilote d’impression local en tant que *pszDriverName* et l’utiliser pour effectuer le rendu au lieu d’utiliser le pilote installé sur l’imprimante serveur à laquelle l’utilisateur est connecté.</span><span class="sxs-lookup"><span data-stu-id="df66a-113">The user can supply a local print driver as *pszDriverName* and use it to do the rendering instead of using the driver installed on the server printer to which the user is connected.</span></span><br/>                                                                                                                                                                                                                                    |
| <span data-ttu-id="df66a-114">\_ \_ \_ Interface utilisateur de connexion à l’imprimante (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="df66a-114">PRINTER\_CONNECTION\_NO\_UI (0x00000040)</span></span>   | <span data-ttu-id="df66a-115">Si cet indicateur de bit est défini, cet appel ne peut pas afficher une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="df66a-115">If this bit-flag is set then this call cannot display a dialog box.</span></span> <span data-ttu-id="df66a-116">Si une boîte de dialogue doit être affichée pour installer un pilote d’imprimante à partir du serveur et que cet indicateur de bit est défini, le pilote d’imprimante n’est pas installé, la connexion d’imprimante n’est pas ajoutée et l’appel échoue.</span><span class="sxs-lookup"><span data-stu-id="df66a-116">If a dialog box must be displayed to install a printer driver from the server and this bit-flag is set, the printer driver will not be installed, the printer connection will not be added, and the call will fail.</span></span><br/> <span data-ttu-id="df66a-117">**Windows 7 :** Dans Windows 7 et les versions ultérieures de Windows, si cet indicateur est défini et que l’utilisateur s’exécute en mode élevé, la boîte de dialogue **faites-vous confiance à cette imprimante ?** ne s’affichera pas.</span><span class="sxs-lookup"><span data-stu-id="df66a-117">**Windows 7:** In Windows 7 and later versions of Windows, if this flag is set and the user is running in elevated mode, the **Do you trust this printer?** dialog will not be shown.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="df66a-118">**pszDriverName**</span><span class="sxs-lookup"><span data-stu-id="df66a-118">**pszDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="df66a-119">Pointeur vers le nom du pilote.</span><span class="sxs-lookup"><span data-stu-id="df66a-119">A pointer to the name of the driver.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df66a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df66a-120">Requirements</span></span>



| <span data-ttu-id="df66a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df66a-121">Requirement</span></span> | <span data-ttu-id="df66a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="df66a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df66a-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df66a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="df66a-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df66a-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="df66a-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df66a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="df66a-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df66a-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="df66a-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="df66a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="df66a-128"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df66a-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df66a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df66a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df66a-130">Impression</span><span class="sxs-lookup"><span data-stu-id="df66a-130">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="df66a-131">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="df66a-131">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




