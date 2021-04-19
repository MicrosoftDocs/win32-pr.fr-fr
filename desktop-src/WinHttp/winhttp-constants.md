---
description: Cette rubrique identifie les constantes utilisées par WinHTTP.
ms.assetid: 460f1463-57a8-47eb-9957-17976757bd7f
title: Constantes WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7c277b4235e23254000766fdef53d25f19ddbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484985"
---
# <a name="winhttp-constants"></a><span data-ttu-id="6bc4f-103">Constantes WinHTTP</span><span class="sxs-lookup"><span data-stu-id="6bc4f-103">WinHTTP Constants</span></span>

<span data-ttu-id="6bc4f-104">WinHTTP utilise les constantes suivantes :</span><span class="sxs-lookup"><span data-stu-id="6bc4f-104">WinHTTP uses the following constants:</span></span>

<dl> <dt>

[<span data-ttu-id="6bc4f-105">**Messages d’erreur**</span><span class="sxs-lookup"><span data-stu-id="6bc4f-105">**Error Messages**</span></span>](error-messages.md)
</dt> <dd>

<span data-ttu-id="6bc4f-106">Messages d’erreur spécifiques aux fonctions WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="6bc4f-106">Error messages specific to the WinHTTP functions.</span></span> <span data-ttu-id="6bc4f-107">Ces fonctions retournent également des messages d’erreur Windows, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="6bc4f-107">These functions also return Windows error messages where appropriate.</span></span> <span data-ttu-id="6bc4f-108">La valeur qui correspond à chaque constante est la valeur de la constante pour les fonctions d’interface de programmation d’applications (API) et les 16 bits inférieurs du numéro d’erreur pour l’objet [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="6bc4f-108">The value that corresponds to each constant is the value of the constant for the application programming interface (API) functions and the lower 16 bits of the error number for the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

</dd> <dt>

[<span data-ttu-id="6bc4f-109">**Codes d’état HTTP**</span><span class="sxs-lookup"><span data-stu-id="6bc4f-109">**HTTP Status Codes**</span></span>](http-status-codes.md)
</dt> <dd>

<span data-ttu-id="6bc4f-110">Les constantes et les valeurs correspondantes qui indiquent les codes d’état HTTP renvoyés par les serveurs sur Internet.</span><span class="sxs-lookup"><span data-stu-id="6bc4f-110">Constants and corresponding values that indicate HTTP status codes returned by servers on the Internet.</span></span>

</dd> <dt>

[<span data-ttu-id="6bc4f-111">**Indicateurs d’option**</span><span class="sxs-lookup"><span data-stu-id="6bc4f-111">**Option Flags**</span></span>](option-flags.md)
</dt> <dd>

<span data-ttu-id="6bc4f-112">Indicateurs d’option pris en charge par [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) et [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span><span class="sxs-lookup"><span data-stu-id="6bc4f-112">Option flags supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span> <span data-ttu-id="6bc4f-113">Tous les indicateurs d’option valides ont une valeur supérieure ou égale à la \_ première \_ option WinHTTP et sont inférieures ou égales à la \_ dernière option WinHTTP \_ .</span><span class="sxs-lookup"><span data-stu-id="6bc4f-113">All valid option flags have a value greater than or equal to WINHTTP\_FIRST\_OPTION and less than or equal to WINHTTP\_LAST\_OPTION.</span></span>

</dd> <dt>

[<span data-ttu-id="6bc4f-114">**\_port Internet**</span><span class="sxs-lookup"><span data-stu-id="6bc4f-114">**INTERNET\_PORT**</span></span>](internet-port.md)
</dt> <dd>

<span data-ttu-id="6bc4f-115">Valeur de mot indiquant le port.</span><span class="sxs-lookup"><span data-stu-id="6bc4f-115">A WORD value indicating the port.</span></span>

</dd> <dt>

[<span data-ttu-id="6bc4f-116">**\_schéma Internet**</span><span class="sxs-lookup"><span data-stu-id="6bc4f-116">**INTERNET\_SCHEME**</span></span>](internet-scheme.md)
</dt> <dd>

<span data-ttu-id="6bc4f-117">Schémas Internet pris en charge par WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="6bc4f-117">Internet schemes supported by WinHTTP.</span></span>

</dd> <dt>

[<span data-ttu-id="6bc4f-118">**Indicateurs d’informations de requête**</span><span class="sxs-lookup"><span data-stu-id="6bc4f-118">**Query Info Flags**</span></span>](query-info-flags.md)
</dt> <dd>

<span data-ttu-id="6bc4f-119">Attributs et modificateurs utilisés par [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="6bc4f-119">Attributes and modifiers used by [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>

</dd> </dl>

 

 



