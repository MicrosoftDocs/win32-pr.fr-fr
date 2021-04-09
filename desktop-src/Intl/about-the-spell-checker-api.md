---
description: Pour les utilisateurs du monde entier, l’entrée textuelle fait partie d’une expérience informatique moderne, pour les blogs, les commentaires, les tweets, la messagerie instantanée ou tout autre type de texte. Dans Windows 8, la vérification orthographique est intégrée pour modifier les contrôles.
ms.assetid: ED569D4F-568B-4381-91C3-8EAEDA4DD47C
title: À propos de l’API vérification orthographique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0d356823e665781052e2a2d5ea98b358155038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866374"
---
# <a name="about-the-spell-checking-api"></a><span data-ttu-id="c9878-104">À propos de l’API vérification orthographique</span><span class="sxs-lookup"><span data-stu-id="c9878-104">About the Spell Checking API</span></span>

<span data-ttu-id="c9878-105">Pour les utilisateurs du monde entier, l’entrée textuelle fait partie d’une expérience informatique moderne, pour les blogs, les commentaires, les tweets, la messagerie instantanée ou tout autre type de texte.</span><span class="sxs-lookup"><span data-stu-id="c9878-105">For users worldwide, textual input is part of a modern computing experience, for blogging, commenting, tweeting, instant messaging, or any other kind of text typing.</span></span> <span data-ttu-id="c9878-106">Dans Windows 8, la vérification orthographique est intégrée pour modifier les contrôles.</span><span class="sxs-lookup"><span data-stu-id="c9878-106">In Windows 8, spell checking is built-in to edit controls.</span></span>

<span data-ttu-id="c9878-107">Les développeurs peuvent utiliser l’API de vérification orthographique dans leurs applications pour utiliser les services de vérification orthographique disponibles.</span><span class="sxs-lookup"><span data-stu-id="c9878-107">Developers can use the spell checking API in their apps to consume available spell checking services.</span></span> <span data-ttu-id="c9878-108">Les développeurs peuvent également créer des vérificateurs d’orthographe qui deviennent des fournisseurs et sont intégrés à l’infrastructure de vérification orthographique Windows.</span><span class="sxs-lookup"><span data-stu-id="c9878-108">Developers can also create spell checkers that become providers and are integrated into the Windows spell checking framework.</span></span>

<span data-ttu-id="c9878-109">L’API vérification orthographique est conçue pour être utilisée par les développeurs professionnels C/C++ des applications COM (Component Object Model) Windows.</span><span class="sxs-lookup"><span data-stu-id="c9878-109">The Spell Checking API is designed for use by professional C/C++ developers of Windows Component Object Model (COM) apps.</span></span> <span data-ttu-id="c9878-110">L’API de vérification orthographique n’est pas prise en charge pour une utilisation dans un service Windows ou ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="c9878-110">The Spell Checking API is not supported for use in a Windows or ASP.NET service.</span></span>

## <a name="versioning"></a><span data-ttu-id="c9878-111">Contrôle de version</span><span class="sxs-lookup"><span data-stu-id="c9878-111">Versioning</span></span>

<span data-ttu-id="c9878-112">L’API vérification orthographique est disponible à partir de Windows 8 ou Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="c9878-112">The Spell Checking API is available beginning with the Windows 8 or Windows Server 2012.</span></span> <span data-ttu-id="c9878-113">Les ajouts ultérieurs à l’API seront gérés en créant de nouvelles interfaces qui peuvent être déterminées à l’aide de [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur les interfaces existantes.</span><span class="sxs-lookup"><span data-stu-id="c9878-113">Future additions to the API will be handled by creating new interfaces that can be determined using [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the existing ones.</span></span>

## <a name="interfaces"></a><span data-ttu-id="c9878-114">Interfaces</span><span class="sxs-lookup"><span data-stu-id="c9878-114">Interfaces</span></span>

<span data-ttu-id="c9878-115">Toutes les interfaces doivent être libérées lorsqu’elles ne sont plus utilisées.</span><span class="sxs-lookup"><span data-stu-id="c9878-115">All interfaces must be released when they are no longer used.</span></span> <span data-ttu-id="c9878-116">Toutes les chaînes **LPWStr** retournées (paramètre de sortie) (et les éléments **LPOLESTR** à partir de [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) doivent être libérées avec [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) quand ils ne sont plus utilisés.</span><span class="sxs-lookup"><span data-stu-id="c9878-116">All returned (out parameter) **LPWSTR** strings (and **LPOLESTR** items from [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) must be released with [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) when no longer used.</span></span>

## <a name="error-handling"></a><span data-ttu-id="c9878-117">Gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="c9878-117">Error handling</span></span>

<span data-ttu-id="c9878-118">Les erreurs sont retournées en tant que **HRESULT** s.</span><span class="sxs-lookup"><span data-stu-id="c9878-118">Errors are returned as **HRESULT** s.</span></span> <span data-ttu-id="c9878-119">[**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) et [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) ne sont pas pris en charge dans cette API.</span><span class="sxs-lookup"><span data-stu-id="c9878-119">[**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) and [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) are not supported in this API.</span></span> <span data-ttu-id="c9878-120">Les erreurs ne sont pas particulièrement exploitables, à l’exception des arguments incorrects.</span><span class="sxs-lookup"><span data-stu-id="c9878-120">Errors are not particularly actionable except for incorrect arguments.</span></span>

<span data-ttu-id="c9878-121">Les codes d’erreur RPC standard peuvent être retournés par l’un des appels d’API, car ils sont hors processus.</span><span class="sxs-lookup"><span data-stu-id="c9878-121">Standard RPC error codes may be returned by any of the API calls because they are out-of-proc.</span></span> <span data-ttu-id="c9878-122">Les délais d’attente RPC standard s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="c9878-122">Standard RPC timeouts apply.</span></span>

## <a name="security"></a><span data-ttu-id="c9878-123">Sécurité</span><span class="sxs-lookup"><span data-stu-id="c9878-123">Security</span></span>

<span data-ttu-id="c9878-124">L’API vérification orthographique peut charger du code externe (vérificateur orthographique).</span><span class="sxs-lookup"><span data-stu-id="c9878-124">The Spell Checking API may load external code (spell check providers).</span></span> <span data-ttu-id="c9878-125">Il exécute ce code hors processus et dans un contexte de sécurité restreint.</span><span class="sxs-lookup"><span data-stu-id="c9878-125">It will run this code out-of-proc and under a restricted security context.</span></span>

## <a name="dictionary-files"></a><span data-ttu-id="c9878-126">Fichiers de dictionnaire</span><span class="sxs-lookup"><span data-stu-id="c9878-126">Dictionary files</span></span>

<span data-ttu-id="c9878-127">Les dictionnaires spécifiques à l’utilisateur pour une langue, qui contiennent le contenu pour les listes de mots ajoutées, exclues et à correction automatique, se trouvent sous% AppData% \\ Microsoft \\ orthographe \\ *<language tag>* .</span><span class="sxs-lookup"><span data-stu-id="c9878-127">The user-specific dictionaries for a language, which hold the content for the Added, Excluded, and AutoCorrect word lists, are located under %AppData%\\Microsoft\\Spelling\\*<language tag>*.</span></span> <span data-ttu-id="c9878-128">Les noms de fichiers sont default. dic (ajouté), default. exclure (excluded) et default. ACL (correction automatique).</span><span class="sxs-lookup"><span data-stu-id="c9878-128">The filenames are default.dic (Added), default.exc (Excluded) and default.acl (AutoCorrect).</span></span> <span data-ttu-id="c9878-129">Les fichiers sont en texte brut UTF-16 qui doit commencer par la marque d’ordre d’octet (BOM) appropriée.</span><span class="sxs-lookup"><span data-stu-id="c9878-129">The files are UTF-16 LE plaintext that must start with the appropriate Byte Order Mark (BOM).</span></span> <span data-ttu-id="c9878-130">Chaque ligne contient un mot (dans les listes de mots ajoutés et exclus) ou une paire de correction automatique avec les mots séparés par une barre verticale (« \| ») (dans la liste de mots correction automatique).</span><span class="sxs-lookup"><span data-stu-id="c9878-130">Each line contains a word (in the Added and Excluded word lists), or an autocorrect pair with the words separated by a vertical bar ("\|") (in the AutoCorrect word list).</span></span> <span data-ttu-id="c9878-131">Les autres fichiers. dic,. exclure et. ACL présents dans l’annuaire seront détectés par le service de vérification orthographique et ajoutés aux listes de mots utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c9878-131">Other .dic, .exc, and .acl files present in the directory will be detected by the spell checking service and added to the user word lists.</span></span> <span data-ttu-id="c9878-132">Ces fichiers sont considérés comme étant en lecture seule et ne sont pas modifiés par l’API de vérification orthographique.</span><span class="sxs-lookup"><span data-stu-id="c9878-132">These files are considered to be read-only and are not modified by the spell checking API.</span></span>

## <a name="installing-a-spell-checking-provider"></a><span data-ttu-id="c9878-133">Installation d’un fournisseur de vérification orthographique</span><span class="sxs-lookup"><span data-stu-id="c9878-133">Installing a spell checking provider</span></span>

<span data-ttu-id="c9878-134">L’installation d’un fournisseur de vérification orthographique doit placer tous les fichiers qu’il utilise dans un emplacement qui autorise l’accès en lecture à partir du SID ([identificateur de sécurité](../secauthz/security-identifiers.md)) « tous les packages d’application ».</span><span class="sxs-lookup"><span data-stu-id="c9878-134">The installation of a spell checking provider must place all the files it uses in a location that allows read access from the SID ([security identifier](../secauthz/security-identifiers.md)) "ALL APPLICATION PACKAGES".</span></span> <span data-ttu-id="c9878-135">Son installation dans un dossier sous « Program Files » fonctionne bien.</span><span class="sxs-lookup"><span data-stu-id="c9878-135">Installing it in a folder under "Program Files" works well.</span></span> <span data-ttu-id="c9878-136">En outre, le fournisseur doit définir certaines clés dans le registre pour qu’il apparaisse à l’API de vérification orthographique.</span><span class="sxs-lookup"><span data-stu-id="c9878-136">Also, the provider must set some keys in the registry for it to appear to the spell checking API.</span></span> <span data-ttu-id="c9878-137">Il peut se trouver dans la ruche HKEY \_ Current \_ User ou la \_ ruche HKEY local machine, \_ selon qu’elle doit être installée uniquement pour l’utilisateur actuel ou pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c9878-137">It can be in either the HKEY\_CURRENT\_USER hive or the HKEY\_LOCAL\_MACHINE hive depending on whether it should install only for the current user or all users.</span></span>


```
Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>
     Default (REG_SZ) = <Name of the provider>

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\InprocServer32
     ThreadingModel (REG_SZ) = "Both"

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\Version
     Version (REG_SZ) = <Version>

Key: <Registry hive>\SOFTWARE\Microsoft\Spelling\Spellers\<Provider id string>
     CLSID (REG_SZ) = <CLSID of the COM Server that implements the provider>
```



<span data-ttu-id="c9878-138">L' [exemple de fournisseur de vérification orthographique](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) fournit un exemple de l’inscription nécessaire pour installer un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c9878-138">The [spell checking provider sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) provides an example of the registration needed to install a provider.</span></span>

<span data-ttu-id="c9878-139">Si vous créez de nouvelles options de vérification orthographique pour un fournisseur de vérification orthographique, consultez [**IOptionDescription :: ID**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) pour obtenir de l’aide sur l’affectation de noms.</span><span class="sxs-lookup"><span data-stu-id="c9878-139">If you are creating new spell checking options for a spell checking provider, see [**IOptionDescription::Id**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) for guidance on naming.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9878-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c9878-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9878-141">Référence de l’API vérification orthographique</span><span class="sxs-lookup"><span data-stu-id="c9878-141">Spell Checking API Reference</span></span>](spell-checker-api-reference.md)
</dt> <dt>

[<span data-ttu-id="c9878-142">Exemple de client de vérification orthographique</span><span class="sxs-lookup"><span data-stu-id="c9878-142">Spell checking client sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerClient)
</dt> <dt>

[<span data-ttu-id="c9878-143">Exemple de fournisseur de vérification orthographique</span><span class="sxs-lookup"><span data-stu-id="c9878-143">Spell checking provider sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider)
</dt> <dt>

[<span data-ttu-id="c9878-144">**IOptionDescription :: ID**</span><span class="sxs-lookup"><span data-stu-id="c9878-144">**IOptionDescription::Id**</span></span>](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id)
</dt> <dt>

[<span data-ttu-id="c9878-145">**IEnumString**</span><span class="sxs-lookup"><span data-stu-id="c9878-145">**IEnumString**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)
</dt> <dt>

<span data-ttu-id="c9878-146">[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="c9878-146">[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span>
</dt> </dl>

 

 
