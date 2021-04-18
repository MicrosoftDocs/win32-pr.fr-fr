---
description: La structure de l’imprimante \_ info \_ 4 spécifie des informations générales sur l’imprimante. La structure peut être utilisée pour récupérer des informations d’imprimante minimales sur un appel à EnumPrinters.
ms.assetid: 81bd0eab-dc1e-4cf1-8f63-3686f1711c1f
title: Structure PRINTER_INFO_4 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_4
- _PRINTER_INFO_4A
- _PRINTER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9a1501008f0235ea303dd1457fc8756c28abc21c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204228"
---
# <a name="printer_info_4-structure"></a><span data-ttu-id="c1cb9-103">Structure de l’imprimante \_ info \_ 4</span><span class="sxs-lookup"><span data-stu-id="c1cb9-103">PRINTER\_INFO\_4 structure</span></span>

<span data-ttu-id="c1cb9-104">La structure de l' **imprimante \_ info \_ 4** spécifie des informations générales sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-104">The **PRINTER\_INFO\_4** structure specifies general printer information.</span></span>

<span data-ttu-id="c1cb9-105">La structure peut être utilisée pour récupérer des informations d’imprimante minimales sur un appel à [**EnumPrinters**](enumprinters.md).</span><span class="sxs-lookup"><span data-stu-id="c1cb9-105">The structure can be used to retrieve minimal printer information on a call to [**EnumPrinters**](enumprinters.md).</span></span> <span data-ttu-id="c1cb9-106">Un tel appel est un moyen simple et rapide de récupérer les noms et les attributs de toutes les imprimantes installées localement sur un système et toutes les connexions d’imprimante distantes qu’un utilisateur a établies.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-106">Such a call is a fast and easy way to retrieve the names and attributes of all locally installed printers on a system and all remote printer connections that a user has established.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1cb9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1cb9-107">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_4 {
  LPTSTR pPrinterName;
  LPTSTR pServerName;
  DWORD  Attributes;
} PRINTER_INFO_4, *PPRINTER_INFO_4;
```



## <a name="members"></a><span data-ttu-id="c1cb9-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c1cb9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c1cb9-109">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="c1cb9-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="c1cb9-110">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’imprimante (locale ou distante).</span><span class="sxs-lookup"><span data-stu-id="c1cb9-110">Pointer to a null-terminated string that specifies the name of the printer (local or remote).</span></span>

</dd> <dt>

<span data-ttu-id="c1cb9-111">**pServerName**</span><span class="sxs-lookup"><span data-stu-id="c1cb9-111">**pServerName**</span></span>
</dt> <dd>

<span data-ttu-id="c1cb9-112">Pointeur vers une chaîne se terminant par un caractère null qui est le nom du serveur.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-112">Pointer to a null-terminated string that is the name of the server.</span></span>

</dd> <dt>

<span data-ttu-id="c1cb9-113">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="c1cb9-113">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="c1cb9-114">Spécifie des informations sur les données retournées.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-114">Specifies information about the returned data.</span></span>



| <span data-ttu-id="c1cb9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1cb9-115">Value</span></span>                       | <span data-ttu-id="c1cb9-116">Signification</span><span class="sxs-lookup"><span data-stu-id="c1cb9-116">Meaning</span></span>                          |
|-----------------------------|----------------------------------|
| <span data-ttu-id="c1cb9-117">\_attribut imprimante \_ local</span><span class="sxs-lookup"><span data-stu-id="c1cb9-117">PRINTER\_ATTRIBUTE\_LOCAL</span></span>   | <span data-ttu-id="c1cb9-118">L’imprimante est une imprimante locale.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-118">The printer is a local printer.</span></span>  |
| <span data-ttu-id="c1cb9-119">attribut d’imprimante \_ \_ réseau</span><span class="sxs-lookup"><span data-stu-id="c1cb9-119">PRINTER\_ATTRIBUTE\_NETWORK</span></span> | <span data-ttu-id="c1cb9-120">L’imprimante est une imprimante distante.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-120">The printer is a remote printer.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1cb9-121">Notes</span><span class="sxs-lookup"><span data-stu-id="c1cb9-121">Remarks</span></span>

<span data-ttu-id="c1cb9-122">La structure **Printer \_ info \_ 4** offre un moyen simple et extrêmement rapide de récupérer les noms des imprimantes installées sur un ordinateur local, ainsi que les connexions distantes qu’un utilisateur a établies.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-122">The **PRINTER\_INFO\_4** structure provides an easy and extremely fast way to retrieve the names of the printers installed on a local machine, as well as the remote connections that a user has established.</span></span> <span data-ttu-id="c1cb9-123">Quand [**EnumPrinters**](enumprinters.md) est appelé avec une structure de données **Printer \_ info \_ 4** , cette fonction interroge le registre pour obtenir les informations spécifiées, puis retourne immédiatement.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-123">When [**EnumPrinters**](enumprinters.md) is called with a **PRINTER\_INFO\_4** data structure, that function queries the registry for the specified information, then returns immediately.</span></span> <span data-ttu-id="c1cb9-124">Cela diffère du comportement de **EnumPrinters** lorsqu’il est appelé avec d’autres niveaux de structures de données d' **informations d’imprimante \_ \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="c1cb9-124">This differs from the behavior of **EnumPrinters** when called with other levels of **PRINTER\_INFO\_xxx** data structures.</span></span> <span data-ttu-id="c1cb9-125">En particulier, quand **EnumPrinters** est appelé avec une structure de données de niveau 2 (**Printer \_ info \_ 2** ), il effectue un appel **OpenPrinter** sur chaque connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-125">In particular, when **EnumPrinters** is called with a level 2 (**PRINTER\_INFO\_2** ) data structure, it performs an **OpenPrinter** call on each remote connection.</span></span> <span data-ttu-id="c1cb9-126">Si une connexion distante est interrompue, si le serveur distant n’existe plus, ou si l’imprimante distante n’existe plus, la fonction doit attendre l’expiration du délai d’attente de RPC et, par conséquent, échouer l’appel **OpenPrinter** .</span><span class="sxs-lookup"><span data-stu-id="c1cb9-126">If a remote connection is down, if the remote server no longer exists, or if the remote printer no longer exists, the function must wait for RPC to time out and consequently fail the **OpenPrinter** call.</span></span> <span data-ttu-id="c1cb9-127">Cette opération peut prendre du temps.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-127">This can take a while.</span></span> <span data-ttu-id="c1cb9-128">Le passage d’une structure **Printer \_ info \_ 4** permet à une application de récupérer un minimum d’informations requises ; si des informations plus détaillées sont souhaitées, un appel **EnumPrinter** de niveau 2 suivant peut être effectué.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-128">Passing a **PRINTER\_INFO\_4** structure lets an application retrieve a bare minimum of required information; if more detailed information is desired, a subsequent **EnumPrinter** level 2 call can be made.</span></span>

<span data-ttu-id="c1cb9-129">Les **attributs** peuvent également contenir des valeurs définies dans le champ **attributs** de **Printer \_ info \_ 2**.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-129">**Attributes** can also contain values that are defined in the **Attributes** field of **PRINTER\_INFO\_2**.</span></span>

<span data-ttu-id="c1cb9-130">Certaines configurations d’imprimante, telles que les connexions d’imprimante à certains serveurs d’impression non Windows, peuvent renvoyer à la fois l’attribut d' **imprimante \_ \_ local** et l' **\_ attribut Printer \_ réseau**.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-130">Some printer configurations, such as printer connections to some non-Windows-based print servers, might return both **PRINTER\_ATTRIBUTE\_LOCAL** and **PRINTER\_ATTRIBUTE\_NETWORK**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1cb9-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1cb9-131">Requirements</span></span>



| <span data-ttu-id="c1cb9-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1cb9-132">Requirement</span></span> | <span data-ttu-id="c1cb9-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1cb9-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1cb9-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1cb9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c1cb9-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1cb9-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c1cb9-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1cb9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c1cb9-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1cb9-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c1cb9-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1cb9-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1cb9-139"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1cb9-139"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c1cb9-140">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="c1cb9-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c1cb9-141">**\_ \_ Infos sur \_ l’imprimante 4W** (Unicode) et **\_ \_ informations sur l’imprimante \_ 4a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c1cb9-141">**\_PRINTER\_INFO\_4W** (Unicode) and **\_PRINTER\_INFO\_4A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="c1cb9-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1cb9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1cb9-143">Impression</span><span class="sxs-lookup"><span data-stu-id="c1cb9-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c1cb9-144">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="c1cb9-144">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="c1cb9-145">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="c1cb9-145">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="c1cb9-146">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="c1cb9-146">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="c1cb9-147">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="c1cb9-147">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="c1cb9-148">**\_Infos sur l’imprimante \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c1cb9-148">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="c1cb9-149">**\_Infos sur l’imprimante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="c1cb9-149">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="c1cb9-150">**\_Infos sur l’imprimante \_ 3**</span><span class="sxs-lookup"><span data-stu-id="c1cb9-150">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> </dl>

 

 




