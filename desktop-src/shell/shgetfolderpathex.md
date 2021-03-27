---
UID: ''
title: SHGetFolderPathEx fonction)
description: Récupère le chemin d’accès d’un dossier connu identifié par KNOWNFOLDERID.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: SHGetFolderPath
ms.topic: reference
req.header: Shlobj.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Shell32.lib
req.dll: API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
api_name:
- SHGetFolderPathEx
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 0dfc3342f3eca5622c25d2df7319cd2323f516ff
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2020
ms.locfileid: "104971659"
---
# <a name="shgetfolderpathex-function"></a><span data-ttu-id="76d13-103">SHGetFolderPathEx fonction)</span><span class="sxs-lookup"><span data-stu-id="76d13-103">SHGetFolderPathEx function</span></span>

## <a name="description"></a><span data-ttu-id="76d13-104">Description</span><span class="sxs-lookup"><span data-stu-id="76d13-104">Description</span></span>

<span data-ttu-id="76d13-105">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="76d13-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span>
<span data-ttu-id="76d13-106">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="76d13-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="76d13-107">Récupère le chemin d’accès complet d’un dossier connu identifié par le [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid)du dossier.</span><span class="sxs-lookup"><span data-stu-id="76d13-107">Retrieves the full path of a known folder identified by the folder's [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid).</span></span>
<span data-ttu-id="76d13-108">Cela étend [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) en vous permettant de définir la taille initiale de la mémoire tampon de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="76d13-108">This extends [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) by allowing you to set the initial size of the string buffer.</span></span>

```cpp
HRESULT WINAPI SHGetFolderPathEx(
  _In_     REFKNOWNFOLDERID rfid,
  _In_     DWORD            dwFlags,
  _In_opt_ HANDLE           hToken,
  _Out_    LPWSTR           pszPath,
  _In_     UINT             cchPath
);
```

## <a name="parameters"></a><span data-ttu-id="76d13-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76d13-109">Parameters</span></span>

### <a name="rfid-in"></a><span data-ttu-id="76d13-110">RFID [in]</span><span class="sxs-lookup"><span data-stu-id="76d13-110">rfid [in]</span></span>

<span data-ttu-id="76d13-111">Référence au **KNOWNFOLDERID** qui identifie le dossier.</span><span class="sxs-lookup"><span data-stu-id="76d13-111">A reference to the **KNOWNFOLDERID** that identifies the folder.</span></span>

### <a name="dwflags-in"></a><span data-ttu-id="76d13-112">dwFlags [in]</span><span class="sxs-lookup"><span data-stu-id="76d13-112">dwFlags [in]</span></span>

<span data-ttu-id="76d13-113">Indicateurs qui spécifient des options de récupération spéciales.</span><span class="sxs-lookup"><span data-stu-id="76d13-113">Flags that specify special retrieval options.</span></span>
<span data-ttu-id="76d13-114">Cette valeur peut être 0 ; Sinon, une ou plusieurs des valeurs [KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag) .</span><span class="sxs-lookup"><span data-stu-id="76d13-114">This value can be 0; otherwise, one or more of the [KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag) values.</span></span>

### <a name="htoken-in-optional"></a><span data-ttu-id="76d13-115">hToken [in, facultatif]</span><span class="sxs-lookup"><span data-stu-id="76d13-115">hToken [in, optional]</span></span>

<span data-ttu-id="76d13-116">[Jeton d’accès](/windows/desktop/SecAuthZ/access-tokens) qui représente un utilisateur particulier.</span><span class="sxs-lookup"><span data-stu-id="76d13-116">An [access token](/windows/desktop/SecAuthZ/access-tokens) that represents a particular user.</span></span>
<span data-ttu-id="76d13-117">Si ce paramètre est **null**, ce qui correspond à l’utilisation la plus courante, la fonction demande le dossier connu pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="76d13-117">If this parameter is **NULL**, which is the most common usage, the function requests the known folder for the current user.</span></span>

<span data-ttu-id="76d13-118">Demandez le dossier d’un utilisateur spécifique en passant le *hToken* de cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="76d13-118">Request a specific user's folder by passing the *hToken* of that user.</span></span>
<span data-ttu-id="76d13-119">Cela s’effectue généralement dans le contexte d’un service qui dispose de privilèges suffisants pour récupérer le jeton d’un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="76d13-119">This is typically done in the context of a service that has sufficient privileges to retrieve the token of a given user.</span></span>
<span data-ttu-id="76d13-120">Ce jeton doit être ouvert avec les droits [TOKEN_QUERY](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) et [TOKEN_IMPERSONATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) .</span><span class="sxs-lookup"><span data-stu-id="76d13-120">That token must be opened with [TOKEN_QUERY](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) and [TOKEN_IMPERSONATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) rights.</span></span>
<span data-ttu-id="76d13-121">Dans certains cas, vous devez également inclure des [TOKEN_DUPLICATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects).</span><span class="sxs-lookup"><span data-stu-id="76d13-121">In some cases, you also need to include [TOKEN_DUPLICATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects).</span></span>
<span data-ttu-id="76d13-122">En plus de transmettre le *hToken* de l’utilisateur, la ruche de registre de cet utilisateur spécifique doit être montée.</span><span class="sxs-lookup"><span data-stu-id="76d13-122">In addition to passing the user's *hToken*, the registry hive of that specific user must be mounted.</span></span>
<span data-ttu-id="76d13-123">Pour plus d’informations sur les problèmes de contrôle d’accès, consultez [Access Control](/windows/desktop/SecAuthZ/access-control) .</span><span class="sxs-lookup"><span data-stu-id="76d13-123">See [Access Control](/windows/desktop/SecAuthZ/access-control) for further discussion of access control issues.</span></span>

<span data-ttu-id="76d13-124">L’attribution du paramètre *hToken* la valeur-1 indique l’utilisateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="76d13-124">Assigning the *hToken* parameter a value of -1 indicates the Default User.</span></span>
<span data-ttu-id="76d13-125">Cela permet aux clients de [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) de trouver des emplacements de dossiers (tels que le dossier **Desktop** ) pour l’utilisateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="76d13-125">This allows clients of [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) to find folder locations (such as the **Desktop** folder) for the Default User.</span></span>
<span data-ttu-id="76d13-126">Le profil utilisateur par défaut est dupliqué lorsqu’un nouveau compte d’utilisateur est créé, et il comprend des dossiers spéciaux tels que **documents** et **Bureau**.</span><span class="sxs-lookup"><span data-stu-id="76d13-126">The Default User user profile is duplicated when any new user account is created, and includes special folders such as **Documents** and **Desktop**.</span></span>
<span data-ttu-id="76d13-127">Tous les éléments ajoutés au dossier utilisateur par défaut apparaissent également dans tout nouveau compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="76d13-127">Any items added to the Default User folder also appear in any new user account.</span></span>
<span data-ttu-id="76d13-128">Notez que l’accès aux dossiers utilisateur par défaut nécessite des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="76d13-128">Note that access to the Default User folders requires administrator privileges.</span></span>

### <a name="pszpath-out"></a><span data-ttu-id="76d13-129">pszPath [out]</span><span class="sxs-lookup"><span data-stu-id="76d13-129">pszPath [out]</span></span>

<span data-ttu-id="76d13-130">Chaîne Unicode terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="76d13-130">A null-terminated, Unicode string.</span></span>
<span data-ttu-id="76d13-131">Cette mémoire tampon doit avoir une taille de cchPath.</span><span class="sxs-lookup"><span data-stu-id="76d13-131">This buffer must be of size cchPath.</span></span>
<span data-ttu-id="76d13-132">Quand **SHGetFolderPathEx** retourne la valeur, ce paramètre contient le chemin d’accès au dossier connu.</span><span class="sxs-lookup"><span data-stu-id="76d13-132">When **SHGetFolderPathEx** returns successfully, this parameter contains the path for the known folder.</span></span>

### <a name="cchpath-in"></a><span data-ttu-id="76d13-133">cchPath [in]</span><span class="sxs-lookup"><span data-stu-id="76d13-133">cchPath [in]</span></span>

<span data-ttu-id="76d13-134">Taille de la mémoire tampon *ppszPath* , en caractères.</span><span class="sxs-lookup"><span data-stu-id="76d13-134">The size of the *ppszPath* buffer, in characters.</span></span>

## <a name="returns"></a><span data-ttu-id="76d13-135">Retours</span><span class="sxs-lookup"><span data-stu-id="76d13-135">Returns</span></span>

<span data-ttu-id="76d13-136">Retourne **S_OK** en cas de réussite, ou une valeur d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="76d13-136">Returns **S_OK** if successful, or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="76d13-137">Notes</span><span class="sxs-lookup"><span data-stu-id="76d13-137">Remarks</span></span>

<span data-ttu-id="76d13-138">Comme [SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) est un wrapper pour [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath), cette fonction (**SHGetFolderPathEx**) sert également d’extension à **SHGetFolderPath**.</span><span class="sxs-lookup"><span data-stu-id="76d13-138">Since [SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) is a wrapper for [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath), this function (**SHGetFolderPathEx**) also serves as an extension to **SHGetFolderPath**.</span></span>

## <a name="see-also"></a><span data-ttu-id="76d13-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76d13-139">See also</span></span>

[<span data-ttu-id="76d13-140">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="76d13-140">KNOWNFOLDERID</span></span>](/windows/desktop/shell/knownfolderid)

[<span data-ttu-id="76d13-141">KNOWN_FOLDER_FLAG</span><span class="sxs-lookup"><span data-stu-id="76d13-141">KNOWN_FOLDER_FLAG</span></span>](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag)

[<span data-ttu-id="76d13-142">SHGetFolderPath</span><span class="sxs-lookup"><span data-stu-id="76d13-142">SHGetFolderPath</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)

[<span data-ttu-id="76d13-143">SHGetKnownFolderIDList</span><span class="sxs-lookup"><span data-stu-id="76d13-143">SHGetKnownFolderIDList</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist)

[<span data-ttu-id="76d13-144">SHGetKnownFolderPath</span><span class="sxs-lookup"><span data-stu-id="76d13-144">SHGetKnownFolderPath</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)
