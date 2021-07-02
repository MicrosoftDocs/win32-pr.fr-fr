---
description: Cette rubrique identifie les constantes utilisées par WinHTTP.
ms.assetid: 460f1463-57a8-47eb-9957-17976757bd7f
title: Constantes WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e37b0e4de7aa3df5e155933bea2be25386c1637
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113175003"
---
# <a name="winhttp-constants"></a><span data-ttu-id="4a39f-103">Constantes WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4a39f-103">WinHTTP Constants</span></span>

<span data-ttu-id="4a39f-104">WinHTTP utilise les constantes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4a39f-104">WinHTTP uses the following constants:</span></span>

<dl>

<dt>

[<span data-ttu-id="4a39f-105">**Messages d'erreur**</span><span class="sxs-lookup"><span data-stu-id="4a39f-105">**Error Messages**</span></span>](error-messages.md)
</dt> <dd>

<span data-ttu-id="4a39f-106">Messages d’erreur spécifiques aux fonctions WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="4a39f-106">Error messages specific to the WinHTTP functions.</span></span> <span data-ttu-id="4a39f-107">ces fonctions retournent également Windows des messages d’erreur, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="4a39f-107">These functions also return Windows error messages where appropriate.</span></span> <span data-ttu-id="4a39f-108">La valeur qui correspond à chaque constante est la valeur de la constante pour les fonctions d’interface de programmation d’applications (API) et les 16 bits inférieurs du numéro d’erreur pour l’objet [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="4a39f-108">The value that corresponds to each constant is the value of the constant for the application programming interface (API) functions and the lower 16 bits of the error number for the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

</dd> <dt>

[<span data-ttu-id="4a39f-109">**Codes d’état HTTP**</span><span class="sxs-lookup"><span data-stu-id="4a39f-109">**HTTP Status Codes**</span></span>](http-status-codes.md)
</dt> <dd>

<span data-ttu-id="4a39f-110">Les constantes et les valeurs correspondantes qui indiquent les codes d’état HTTP renvoyés par les serveurs sur Internet.</span><span class="sxs-lookup"><span data-stu-id="4a39f-110">Constants and corresponding values that indicate HTTP status codes returned by servers on the Internet.</span></span>

</dd> <dt>

[<span data-ttu-id="4a39f-111">**Indicateurs d’option**</span><span class="sxs-lookup"><span data-stu-id="4a39f-111">**Option Flags**</span></span>](option-flags.md)
</dt> <dd>

<span data-ttu-id="4a39f-112">Indicateurs d’option pris en charge par [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) et [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span><span class="sxs-lookup"><span data-stu-id="4a39f-112">Option flags supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span> <span data-ttu-id="4a39f-113">Tous les indicateurs d’option valides ont une valeur supérieure ou égale à la \_ première \_ option WinHTTP et sont inférieures ou égales à la \_ dernière option WinHTTP \_ .</span><span class="sxs-lookup"><span data-stu-id="4a39f-113">All valid option flags have a value greater than or equal to WINHTTP\_FIRST\_OPTION and less than or equal to WINHTTP\_LAST\_OPTION.</span></span>

</dd> <dt>

[<span data-ttu-id="4a39f-114">**\_port Internet**</span><span class="sxs-lookup"><span data-stu-id="4a39f-114">**INTERNET\_PORT**</span></span>](internet-port.md)
</dt> <dd>

<span data-ttu-id="4a39f-115">Valeur de mot indiquant le port.</span><span class="sxs-lookup"><span data-stu-id="4a39f-115">A WORD value indicating the port.</span></span>

</dd> <dt>

[<span data-ttu-id="4a39f-116">**\_schéma Internet**</span><span class="sxs-lookup"><span data-stu-id="4a39f-116">**INTERNET\_SCHEME**</span></span>](internet-scheme.md)
</dt> <dd>

<span data-ttu-id="4a39f-117">Schémas Internet pris en charge par WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="4a39f-117">Internet schemes supported by WinHTTP.</span></span>

</dd>

<dt>

[<span data-ttu-id="4a39f-118">**Indicateurs d’informations de requête**</span><span class="sxs-lookup"><span data-stu-id="4a39f-118">**Query Info Flags**</span></span>](query-info-flags.md)
</dt>
<dd>

<span data-ttu-id="4a39f-119">Attributs et modificateurs utilisés par [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="4a39f-119">Attributes and modifiers used by [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>
</dd>

<dt>

<span data-ttu-id="4a39f-120">**WINHTTP_EXTENDED_HEADER_FLAG_UNICODE**</span><span class="sxs-lookup"><span data-stu-id="4a39f-120">**WINHTTP_EXTENDED_HEADER_FLAG_UNICODE**</span></span>
</dt>
<dd>

<span data-ttu-id="4a39f-121">A la valeur 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="4a39f-121">Has a value of 0x00000001.</span></span> <span data-ttu-id="4a39f-122">Indique à [WinHttpAddRequestHeadersEx](/windows/win32/api/winhttp/nf-winhttp-winhttpaddrequestheadersex) que les chaînes passées sont des chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="4a39f-122">Indicates to [WinHttpAddRequestHeadersEx](/windows/win32/api/winhttp/nf-winhttp-winhttpaddrequestheadersex) that the strings passed in are Unicode strings.</span></span>
</dd>

<dt>

<span data-ttu-id="4a39f-123">**WINHTTP_READ_DATA_EX_FLAG_FILL_BUFFER**</span><span class="sxs-lookup"><span data-stu-id="4a39f-123">**WINHTTP_READ_DATA_EX_FLAG_FILL_BUFFER**</span></span>
</dt>
<dd>

<span data-ttu-id="4a39f-124">A la valeur 0x0000000000000001ull.</span><span class="sxs-lookup"><span data-stu-id="4a39f-124">Has a value of 0x0000000000000001ull.</span></span> <span data-ttu-id="4a39f-125">Ordonne à [WinHttpReadDataEx](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddataex) de ne pas terminer l’appel tant que le tampon de données fourni n’a pas été rempli ou que la réponse n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="4a39f-125">Instructs [WinHttpReadDataEx](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddataex) not to complete the call until the provided data buffer has been filled, or the response is complete.</span></span> <span data-ttu-id="4a39f-126">Le passage de cet indicateur rend le comportement de **WinHttpReadDataEx** équivalent à celui de [WinHttpReadData](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata).</span><span class="sxs-lookup"><span data-stu-id="4a39f-126">Passing this flag makes the behavior of **WinHttpReadDataEx** equivalent to that of [WinHttpReadData](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata).</span></span>
</dd>

</dl>
