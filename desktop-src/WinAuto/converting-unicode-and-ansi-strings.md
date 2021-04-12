---
title: Conversion de chaînes Unicode et ANSI
description: Microsoft Active Accessibility utilise des chaînes Unicode telles que définies par le type de données BSTR.
ms.assetid: 47f525fe-6d18-43b9-a706-e49afa796830
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fa26813c61be0a3959593f370016cfce0211ea9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315785"
---
# <a name="converting-unicode-and-ansi-strings"></a><span data-ttu-id="df3cf-103">Conversion de chaînes Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="df3cf-103">Converting Unicode and ANSI Strings</span></span>

<span data-ttu-id="df3cf-104">Microsoft Active Accessibility utilise des chaînes Unicode telles que définies par le type de données **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="df3cf-104">Microsoft Active Accessibility uses Unicode strings as defined by the **BSTR** data type.</span></span> <span data-ttu-id="df3cf-105">Si votre application n’utilise pas de chaînes Unicode, ou si vous souhaitez convertir des chaînes pour certains appels d’API, utilisez les fonctions de Microsoft Win32 [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) et [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) pour effectuer la conversion nécessaire.</span><span class="sxs-lookup"><span data-stu-id="df3cf-105">If your application does not use Unicode strings, or if you want to convert strings for certain API calls, use the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) and [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) Microsoft Win32 functions to perform the necessary conversion.</span></span>

<span data-ttu-id="df3cf-106">Utilisez [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) pour convertir une chaîne Unicode en une chaîne ANSI.</span><span class="sxs-lookup"><span data-stu-id="df3cf-106">Use [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) to convert a Unicode string to an ANSI string.</span></span> <span data-ttu-id="df3cf-107">La fonction [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) convertit une chaîne ANSI en chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="df3cf-107">The [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function converts an ANSI string to a Unicode string.</span></span>

<span data-ttu-id="df3cf-108">Utilisez [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) et [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) pour allouer et libérer des types de données **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="df3cf-108">Use [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) and [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) to allocate and free **BSTR** data types.</span></span>

<span data-ttu-id="df3cf-109">Pour plus d’informations sur ces fonctions de chaîne, consultez leurs références dans le kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="df3cf-109">For more information about these string functions, see their references in the Windows Software Development Kit (SDK).</span></span>

 

 