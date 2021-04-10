---
title: Public et exemple de code
description: Cette rubrique décrit les groupes de développeurs pour lesquels l’interface d’analyse anti-programme malveillant est conçue.
ms.topic: article
ms.date: 03/20/2019
ms.openlocfilehash: 22cf1156a8fa0aedc212b2ab70e34b984d13470f
ms.sourcegitcommit: 272ba17a215d0d27bb7918fee1192d4954ccc576
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2020
ms.locfileid: "104030727"
---
# <a name="developer-audience-and-sample-code"></a><span data-ttu-id="8e86e-103">Public et exemple de code</span><span class="sxs-lookup"><span data-stu-id="8e86e-103">Developer audience, and sample code</span></span>

<span data-ttu-id="8e86e-104">L’interface d’analyse anti-programme malveillant est conçue pour être utilisée par deux groupes de développeurs.</span><span class="sxs-lookup"><span data-stu-id="8e86e-104">The Antimalware Scan Interface is designed for use by two groups of developers.</span></span>

- <span data-ttu-id="8e86e-105">Les développeurs d’applications qui souhaitent effectuer des demandes aux produits anti-programme malveillant à partir de leurs applications.</span><span class="sxs-lookup"><span data-stu-id="8e86e-105">Application developers who want to make requests to antimalware products from within their apps.</span></span>
- <span data-ttu-id="8e86e-106">Créateurs de logiciels anti-programmes malveillants tiers qui souhaitent que leurs produits offrent les meilleures fonctionnalités aux applications.</span><span class="sxs-lookup"><span data-stu-id="8e86e-106">Third-party creators of antimalware products who want their products to offer the best features to applications.</span></span>

## <a name="application-developers"></a><span data-ttu-id="8e86e-107">Développeurs d’applications</span><span class="sxs-lookup"><span data-stu-id="8e86e-107">Application developers</span></span>

<span data-ttu-id="8e86e-108">AMSI est conçu en particulier pour combattre les « programmes malveillants en fichier ».</span><span class="sxs-lookup"><span data-stu-id="8e86e-108">AMSI is designed in particular to combat "fileless malware".</span></span> <span data-ttu-id="8e86e-109">Les types d’applications qui peuvent tirer le meilleur parti de la technologie AMSI incluent les moteurs de script, les applications qui ont besoin de mémoires tampons pour être analysés avant de les utiliser, et les applications qui traitent des fichiers pouvant contenir du code exécutable non PE (par exemple, des macros Microsoft Word et Excel ou des documents PDF).</span><span class="sxs-lookup"><span data-stu-id="8e86e-109">Application types that can optimally leverage AMSI technology include script engines, applications that need memory buffers to be scanned before using them, and applications that process files that can contain non-PE executable code (such as Microsoft Word and Excel macros, or PDF documents).</span></span> <span data-ttu-id="8e86e-110">Toutefois, l’utilité de la technologie AMSI n’est pas limitée à ces exemples.</span><span class="sxs-lookup"><span data-stu-id="8e86e-110">However, the usefulness of AMSI technology is not limited to those examples.</span></span>

<span data-ttu-id="8e86e-111">Il existe deux façons d’interagir avec AMSI dans votre application.</span><span class="sxs-lookup"><span data-stu-id="8e86e-111">There are two ways in which you can interface with AMSI in your application.</span></span>

- <span data-ttu-id="8e86e-112">À l’aide des API Win32 AMSI.</span><span class="sxs-lookup"><span data-stu-id="8e86e-112">By using the AMSI Win32 APIs.</span></span> <span data-ttu-id="8e86e-113">Voir [fonctions de l’interface d’analyse anti-programme malveillant (AMSI)](/windows/desktop/amsi/antimalware-scan-interface-functions).</span><span class="sxs-lookup"><span data-stu-id="8e86e-113">See [Antimalware Scan Interface (AMSI) functions](/windows/desktop/amsi/antimalware-scan-interface-functions).</span></span>
- <span data-ttu-id="8e86e-114">À l’aide des interfaces COM AMSI.</span><span class="sxs-lookup"><span data-stu-id="8e86e-114">By using the AMSI COM interfaces.</span></span> <span data-ttu-id="8e86e-115">Voir [interface **IAmsiStream**](/windows/desktop/api/amsi/nn-amsi-iamsistream).</span><span class="sxs-lookup"><span data-stu-id="8e86e-115">See [**IAmsiStream** interface](/windows/desktop/api/amsi/nn-amsi-iamsistream).</span></span>

<span data-ttu-id="8e86e-116">Pour obtenir un exemple de code illustrant l’utilisation de AMSI dans votre application COM, consultez l' [exemple d’application IAmsiStream interface](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).</span><span class="sxs-lookup"><span data-stu-id="8e86e-116">For sample code showing how to consume AMSI within your COM application, see the [IAmsiStream interface sample application](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).</span></span>

## <a name="third-party-creators-of-antimalware-products"></a><span data-ttu-id="8e86e-117">Créateurs de logiciels anti-programme malveillant tiers</span><span class="sxs-lookup"><span data-stu-id="8e86e-117">Third-party creators of antimalware products</span></span>

<span data-ttu-id="8e86e-118">En tant que créateur de produits anti-programme malveillant, vous pouvez choisir de créer et d’inscrire votre propre serveur COM in-process (une DLL) pour qu’il fonctionne en tant que fournisseur AMSI.</span><span class="sxs-lookup"><span data-stu-id="8e86e-118">As a creator of antimalware products, you can choose to author and register your own in-process COM server (a DLL) to function as an AMSI provider.</span></span> <span data-ttu-id="8e86e-119">Ce fournisseur AMSI doit implémenter l' [interface **IAntimalwareProvider**](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider)et doit s’exécuter in-process.</span><span class="sxs-lookup"><span data-stu-id="8e86e-119">That AMSI provider must implement the [**IAntimalwareProvider** interface](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider), and it must run in-process.</span></span>

<span data-ttu-id="8e86e-120">Notez que, après Windows 10, version 1709 (la mise à jour d’automne 2017 Creators), votre DLL de fournisseur AMSI peut ne pas fonctionner si cela dépend d’autres dll dans son chemin d’accès à charger en même temps.</span><span class="sxs-lookup"><span data-stu-id="8e86e-120">Note that, after Windows 10, version 1709 (the Fall 2017 Creators' Update), your AMSI provider DLL may not work if it depends upon other DLLs in its path to be loaded at the same time.</span></span> <span data-ttu-id="8e86e-121">Pour empêcher le détournement de DLL, nous recommandons que votre DLL de fournisseur charge explicitement ses dépendances (avec un chemin d’accès complet) à l’aide d’appels [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) sécurisés, ou d’un équivalent.</span><span class="sxs-lookup"><span data-stu-id="8e86e-121">To prevent DLL hijacking, we recommend that your provider DLL load its dependencies explicitly (with a full path) using secure [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) calls, or equivalent.</span></span> <span data-ttu-id="8e86e-122">Nous vous recommandons de le faire au lieu de vous appuyer sur le comportement de recherche **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="8e86e-122">We recommend this instead of relying on the **LoadLibrary** search behavior.</span></span>

<span data-ttu-id="8e86e-123">La section ci-dessous montre comment inscrire votre fournisseur AMSI.</span><span class="sxs-lookup"><span data-stu-id="8e86e-123">The section below shows how to register your AMSI provider.</span></span> <span data-ttu-id="8e86e-124">Pour obtenir un exemple de code complet illustrant comment créer votre propre DLL de fournisseur AMSI, consultez l' [exemple d’application IAntimalwareProvider interface](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).</span><span class="sxs-lookup"><span data-stu-id="8e86e-124">For full sample code showing how to author your own AMSI provider DLL, see the [IAntimalwareProvider interface sample application](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).</span></span>

### <a name="register-your-provider-dll-with-amsi"></a><span data-ttu-id="8e86e-125">Inscrire votre DLL de fournisseur auprès de AMSI</span><span class="sxs-lookup"><span data-stu-id="8e86e-125">Register your provider DLL with AMSI</span></span>

<span data-ttu-id="8e86e-126">Pour commencer, vous devez vous assurer que ces clés de Registre Windows existent.</span><span class="sxs-lookup"><span data-stu-id="8e86e-126">To begin with, you need to ensure that these Windows Registry keys exist.</span></span>

- <span data-ttu-id="8e86e-127">HKLM\SOFTWARE\Microsoft\AMSI\Providers</span><span class="sxs-lookup"><span data-stu-id="8e86e-127">HKLM\SOFTWARE\Microsoft\AMSI\Providers</span></span>
- <span data-ttu-id="8e86e-128">HKLM\SOFTWARE\Classes\CLSID</span><span class="sxs-lookup"><span data-stu-id="8e86e-128">HKLM\SOFTWARE\Classes\CLSID</span></span>

<span data-ttu-id="8e86e-129">Un fournisseur AMSI est un serveur COM in-process.</span><span class="sxs-lookup"><span data-stu-id="8e86e-129">An AMSI provider is an in-process COM server.</span></span> <span data-ttu-id="8e86e-130">Par conséquent, il doit s’inscrire auprès de COM.</span><span class="sxs-lookup"><span data-stu-id="8e86e-130">Consequently, it needs to register itself with COM.</span></span> <span data-ttu-id="8e86e-131">Les classes COM sont inscrites dans `HKLM\SOFTWARE\Classes\CLSID` .</span><span class="sxs-lookup"><span data-stu-id="8e86e-131">COM classes are registered in `HKLM\SOFTWARE\Classes\CLSID`.</span></span>

<span data-ttu-id="8e86e-132">Le code ci-dessous montre comment inscrire un fournisseur AMSI dont le GUID (pour cet exemple) est `2E5D8A62-77F9-4F7B-A90C-2744820139B2` .</span><span class="sxs-lookup"><span data-stu-id="8e86e-132">The code below shows how to register an AMSI provider, whose GUID (for this example) we will assume is `2E5D8A62-77F9-4F7B-A90C-2744820139B2`.</span></span>

```cpp
#include <strsafe.h>
...
HRESULT SetKeyStringValue(_In_ HKEY key, _In_opt_ PCWSTR subkey, _In_opt_ PCWSTR valueName, _In_ PCWSTR stringValue)
{
    LONG status = RegSetKeyValue(key, subkey, valueName, REG_SZ, stringValue, (wcslen(stringValue) + 1) * sizeof(wchar_t));
    return HRESULT_FROM_WIN32(status);
}

STDAPI DllRegisterServer()
{
    wchar_t modulePath[MAX_PATH];
    if (GetModuleFileName(g_currentModule, modulePath, ARRAYSIZE(modulePath)) >= ARRAYSIZE(modulePath))
    {
        return E_UNEXPECTED;
    }

    // Create a standard COM registration for our CLSID.
    // The class must be registered as "Both" threading model,
    // and support multithreaded access.
    wchar_t clsidString[40];
    if (StringFromGUID2(__uuidof(SampleAmsiProvider), clsidString, ARRAYSIZE(clsidString)) == 0)
    {
        return E_UNEXPECTED;
    }

    wchar_t keyPath[200];
    HRESULT hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Classes\\CLSID\\%ls", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, L"SampleAmsiProvider");
    if (FAILED(hr)) return hr;

    hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Classes\\CLSID\\%ls\\InProcServer32", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, modulePath);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, L"ThreadingModel", L"Both");
    if (FAILED(hr)) return hr;

    // Register this CLSID as an anti-malware provider.
    hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Microsoft\\AMSI\\Providers\\%ls", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, L"SampleAmsiProvider");
    if (FAILED(hr)) return hr;

    return S_OK;
}
```

<span data-ttu-id="8e86e-133">Si votre DLL implémente la [fonction DllRegisterServer](/windows/desktop/api/olectl/nf-olectl-dllregisterserver), comme l’illustre l’exemple ci-dessus, vous pouvez l’inscrire à l’aide de l’exécutable fourni par Windows `regsvr32.exe` .</span><span class="sxs-lookup"><span data-stu-id="8e86e-133">If your DLL implements the [DllRegisterServer function](/windows/desktop/api/olectl/nf-olectl-dllregisterserver), as the example above does, then you can register it by using the Windows-supplied executable `regsvr32.exe`.</span></span> <span data-ttu-id="8e86e-134">À partir d’une invite de commandes avec élévation de privilèges, émettez une commande de ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="8e86e-134">From an elevated command prompt, issue a command of this form.</span></span>

```cmd
C:>C:\Windows\System32\regsvr32.exe SampleAmsiProvider.dll
```

<span data-ttu-id="8e86e-135">Dans cet exemple, la commande crée les entrées suivantes.</span><span class="sxs-lookup"><span data-stu-id="8e86e-135">In this example, the command creates the following entries.</span></span>

<span data-ttu-id="8e86e-136">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span><span class="sxs-lookup"><span data-stu-id="8e86e-136">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\{2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span></span>

<span data-ttu-id="8e86e-137">&nbsp;&nbsp;&nbsp;&nbsp;**Valeurs    REG_SZ exemple d’implémentation de fournisseur AMSI**</span><span class="sxs-lookup"><span data-stu-id="8e86e-137">&nbsp;&nbsp;&nbsp;&nbsp;**(Default)    REG_SZ    Sample AMSI Provider implementation**</span></span>


<span data-ttu-id="8e86e-138">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2} \InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="8e86e-138">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\{2E5D8A62-77F9-4F7B-A90C-2744820139B2}\InprocServer32**</span></span>

<span data-ttu-id="8e86e-139">&nbsp;&nbsp;&nbsp;&nbsp;**Valeurs    REG_EXPAND_SZ% ProgramFiles% \TestProvider\SampleAmsiProvider.dll**</span><span class="sxs-lookup"><span data-stu-id="8e86e-139">&nbsp;&nbsp;&nbsp;&nbsp;**(Default)    REG_EXPAND_SZ    %ProgramFiles%\TestProvider\SampleAmsiProvider.dll**</span></span>

<span data-ttu-id="8e86e-140">&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel REG_SZ les deux**</span><span class="sxs-lookup"><span data-stu-id="8e86e-140">&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel    REG_SZ    Both**</span></span>

<span data-ttu-id="8e86e-141">En plus de l’inscription COM standard, vous devez également inscrire le fournisseur auprès de AMSI.</span><span class="sxs-lookup"><span data-stu-id="8e86e-141">In addition to regular COM registration, you also need to enroll the provider with AMSI.</span></span> <span data-ttu-id="8e86e-142">Pour ce faire, ajoutez une entrée à la clé suivante.</span><span class="sxs-lookup"><span data-stu-id="8e86e-142">You do that by adding an entry to the following key.</span></span>

<span data-ttu-id="8e86e-143">**HKLM\SOFTWARE\Microsoft\AMSI\Providers**</span><span class="sxs-lookup"><span data-stu-id="8e86e-143">**HKLM\SOFTWARE\Microsoft\AMSI\Providers**</span></span>

<span data-ttu-id="8e86e-144">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="8e86e-144">For example,</span></span>

<span data-ttu-id="8e86e-145">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span><span class="sxs-lookup"><span data-stu-id="8e86e-145">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\{2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span></span>
