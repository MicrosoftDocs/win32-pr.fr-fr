---
title: Prise en charge des IDN dans WinINet
description: À compter de Windows Server 2008 et Windows Vista, la partie hôte de l’URL Unicode est convertie en nom de domaine international (IDN, Internationalized Domain Name).
ms.assetid: 7c56908e-f6d0-48dc-9ac1-73f888fb7b6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510b1bc8d2ab77534d7f5dac587f287d5e7095af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382591"
---
# <a name="idn-support-in-wininet"></a><span data-ttu-id="82343-103">Prise en charge des IDN dans WinINet</span><span class="sxs-lookup"><span data-stu-id="82343-103">IDN Support in WinINet</span></span>

<span data-ttu-id="82343-104">À compter de Windows Server 2008 et Windows Vista, la partie hôte de l’URL Unicode est convertie en nom de domaine international (IDN, Internationalized Domain Name).</span><span class="sxs-lookup"><span data-stu-id="82343-104">Starting in Windows Server 2008 and Windows Vista, the host portion of the Unicode URL is converted to the Internationalized Domain Name (IDN).</span></span> <span data-ttu-id="82343-105">Des parties distinctes de l’encodage d’URL Unicode peuvent également être modifiées par des configurations définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="82343-105">Separate portions of the Unicode URL encoding can also be modified by configurations set by the application.</span></span> <span data-ttu-id="82343-106">Les versions ANSI de l’API WinINet continuent à envoyer l’URL sur le réseau telle qu’elle est entrée par l’application. Toutefois, les versions Unicode WinINet de l’API sont désormais conformes à la norme IDN (RFC3490) pour les encodages d’URL.</span><span class="sxs-lookup"><span data-stu-id="82343-106">The ANSI versions of the WinINet API continue to send the URL over the wire as entered by the application, however the WinINet Unicode versions of the API now conform to the IDN standard (RFC3490) for URL encodings.</span></span>

<span data-ttu-id="82343-107">Par défaut, lorsqu’une URL est entrée en tant que paramètre Unicode, la partie hôte, pour les connexions proxy et directes, est convertie au format IDN.</span><span class="sxs-lookup"><span data-stu-id="82343-107">By default, when a URL is entered as a Unicode parameter, the host portion, for both proxy and direct connections, is converted to IDN format.</span></span> <span data-ttu-id="82343-108">L’application a la possibilité de désactiver la mise en forme de l’hôte IDN en définissant l’option **Internet \_ \_ IDN** .</span><span class="sxs-lookup"><span data-stu-id="82343-108">The application has the option to disable IDN host formatting by setting the **INTERNET\_OPTION\_IDN** option.</span></span> <span data-ttu-id="82343-109">La conversion de l’hôte IDN peut être activée uniquement sur les connexions directes ou proxy à l’aide de l’indicateur Internet indicateurs de **\_ \_ \_ proxy** IDN **\_ \_ \_ direct** ou Internet indicateur IDN avec l' **\_ option Internet \_ IDN**.</span><span class="sxs-lookup"><span data-stu-id="82343-109">IDN host conversion can be enabled on only the direct or proxy connections by using the **INTERNET\_FLAG\_IDN\_DIRECT** or **INTERNET\_FLAG\_IDN\_PROXY** flags with **INTERNET\_OPTION\_IDN**.</span></span>

<span data-ttu-id="82343-110">L’exemple de code suivant montre comment désactiver la conversion de l’hôte IDN à la fois pour le proxy et pour les connexions directes.</span><span class="sxs-lookup"><span data-stu-id="82343-110">The following code example shows how to disable IDN host conversion for both the proxy and direct connections.</span></span>

``` syntax
DWORD IDN = 0; 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_IDN,
                   &IDN, 
                   sizeof(DWORD) ); 
```

<span data-ttu-id="82343-111">Si la mise en forme de l’hôte IDN est désactivée, l’application a la possibilité de spécifier la page de codes souhaitée à l’aide de la **\_ page de \_ codes d’option Internet**.</span><span class="sxs-lookup"><span data-stu-id="82343-111">If IDN host formatting is disabled, the application has the option to specify the desired codepage using **INTERNET\_OPTION\_CODEPAGE**.</span></span>

<span data-ttu-id="82343-112">L’exemple de code suivant montre comment spécifier la page de codes japonaise.</span><span class="sxs-lookup"><span data-stu-id="82343-112">The following code example shows how to specify the Japanese code page.</span></span>

``` syntax
DWORD CP_SHIFT_JIS = 932;  // ANSI/OEM  Japanese, Shift-JIS
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE,
                   &CP_SHIFT_JIS, 
                   Sizeof(DWORD) ); 
```

<span data-ttu-id="82343-113">La partie du chemin d’accès de l’URL est encodée en UTF8 par défaut, et les autres segments de l’URL, la requête ou le fragment, sont convertis en page de codes système par défaut (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="82343-113">The path portion of the URL is UTF8 encoded by default, and the remaining segments of the URL, the query or fragment, are converted to the default system code page (CP\_ACP).</span></span>

<span data-ttu-id="82343-114">L’exemple suivant montre comment spécifier la page de codes de langue coréenne pour la partie chemin d’accès de l’URL.</span><span class="sxs-lookup"><span data-stu-id="82343-114">The following example shows how to specify the Korean language code page for the path portion of the URL.</span></span>

``` syntax
DWORD CP_KOREAN = 949;   // ANSI/OEM Korean 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE_PATH,
                   &CP_KOREAN, 
                   sizeof(DWORD) );
```

<span data-ttu-id="82343-115">Le tableau suivant définit les options qui prennent en charge l’IDN.</span><span class="sxs-lookup"><span data-stu-id="82343-115">The following table defines the options that support IDN.</span></span> <span data-ttu-id="82343-116">Pour plus d’informations, consultez la rubrique [indicateurs d’option](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="82343-116">For more information, see the [Option Flags](option-flags.md) topic.</span></span>



| <span data-ttu-id="82343-117">Option</span><span class="sxs-lookup"><span data-stu-id="82343-117">Option</span></span>                            | <span data-ttu-id="82343-118">Description</span><span class="sxs-lookup"><span data-stu-id="82343-118">Description</span></span>                                                                                                                                                                                                                     |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82343-119">page de codes de l' \_ option Internet \_</span><span class="sxs-lookup"><span data-stu-id="82343-119">INTERNET\_OPTION\_CODEPAGE</span></span>        | <span data-ttu-id="82343-120">Cette option est définie sur la demande, ou sur le descripteur de connexion, pour spécifier un schéma d’encodage de page de codes pour la partie hôte de l’URL.</span><span class="sxs-lookup"><span data-stu-id="82343-120">This option is set on the request, or connection handle, to specify a code page encoding scheme for the host portion of the URL.</span></span> <span data-ttu-id="82343-121">Cette option est ignorée si l’IDN est activé.</span><span class="sxs-lookup"><span data-stu-id="82343-121">This option is ignored if IDN is enabled.</span></span>                                                      |
| <span data-ttu-id="82343-122">chemin de la page de codes de l' \_ option Internet \_ \_</span><span class="sxs-lookup"><span data-stu-id="82343-122">INTERNET\_OPTION\_CODEPAGE\_PATH</span></span>  | <span data-ttu-id="82343-123">Cette option est définie sur la demande, ou le descripteur de connexion active le schéma d’encodage spécifié pour la partie chemin d’accès de l’URL.</span><span class="sxs-lookup"><span data-stu-id="82343-123">This option is set on the request, or connection handle enables the specified encoding scheme for the path portion of the URL.</span></span> <span data-ttu-id="82343-124">Par défaut, la partie chemin d’accès de l’URL est encodée en UTF8.</span><span class="sxs-lookup"><span data-stu-id="82343-124">By default, the path portion of the URL is UTF8 encoded.</span></span>                                         |
| <span data-ttu-id="82343-125">page de codes de l' \_ option Internet \_ \_ extra</span><span class="sxs-lookup"><span data-stu-id="82343-125">INTERNET\_OPTION\_CODEPAGE\_EXTRA</span></span> | <span data-ttu-id="82343-126">La définition de cette option sur la demande, ou le descripteur de connexion active le schéma d’encodage spécifié pour la partie supplémentaire de l’URL.</span><span class="sxs-lookup"><span data-stu-id="82343-126">Setting this option on the request, or connection handle enables the specified encoding scheme for the extra portion of the URL.</span></span> <span data-ttu-id="82343-127">Par défaut, la partie supplémentaire de l’URL est encodée dans la page de codes système par défaut (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="82343-127">By default, the extra portion of the URL is encoded in the default system code page (CP\_ACP).</span></span> |
| <span data-ttu-id="82343-128">\_IDN des options Internet \_</span><span class="sxs-lookup"><span data-stu-id="82343-128">INTERNET\_OPTION\_IDN</span></span>             | <span data-ttu-id="82343-129">Cette option peut être utilisée sur la demande ou sur le descripteur de connexion pour activer ou désactiver la conversion de l’hôte IDN.</span><span class="sxs-lookup"><span data-stu-id="82343-129">This option can be used on the request, or connection handle to enable or disable IDN host conversion.</span></span> <span data-ttu-id="82343-130">Lorsque l’IDN est désactivé, WinINet utilise la page de codes par défaut du système pour encoder la partie hôte ou autorité de l’URL.</span><span class="sxs-lookup"><span data-stu-id="82343-130">When IDN is disabled, WinINet uses the default system codepage to encode the host or authority portion of the URL.</span></span>       |



 

> [!Note]  
> <span data-ttu-id="82343-131">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="82343-131">WinINet does not support server implementations.</span></span> <span data-ttu-id="82343-132">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="82343-132">In addition, it should not be used from a service.</span></span> <span data-ttu-id="82343-133">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="82343-133">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 