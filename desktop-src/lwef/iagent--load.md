---
title: Charge IAgent
description: Charge IAgent
ms.assetid: 8f25e6b6-a117-4b37-969a-d8f80c7be224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ce2835d60f3edce6f45d181927437ba6e58b18
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120932"
---
# <a name="iagentload"></a><span data-ttu-id="f83b8-103">IAgent :: Load</span><span class="sxs-lookup"><span data-stu-id="f83b8-103">IAgent::Load</span></span>

<span data-ttu-id="f83b8-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f83b8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Load(
   VARIANT vLoadKey,  // data provider
   long * pdwCharID,  // address of a variable for character ID
   long * pdwReqID    // address of a variable for request ID
);
```

<span data-ttu-id="f83b8-105">Charge un caractère dans la collection de [**caractères**](./iagent.md) .</span><span class="sxs-lookup"><span data-stu-id="f83b8-105">Loads a character into the [**Characters**](./iagent.md) collection.</span></span>

-   <span data-ttu-id="f83b8-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="f83b8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f83b8-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*</span><span class="sxs-lookup"><span data-stu-id="f83b8-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*</span></span>
</dt> <dd>

<span data-ttu-id="f83b8-108">Un type de données Variant qui doit être l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="f83b8-108">A variant datatype that must be one of the following:</span></span>



| <span data-ttu-id="f83b8-109">Value</span><span class="sxs-lookup"><span data-stu-id="f83b8-109">Value</span></span>           | <span data-ttu-id="f83b8-110">Description</span><span class="sxs-lookup"><span data-stu-id="f83b8-110">Description</span></span>                                                                      |
|------------|-----------------------------------------------------------------------|
| <span data-ttu-id="f83b8-111">*filespec*</span><span class="sxs-lookup"><span data-stu-id="f83b8-111">*filespec*</span></span> | <span data-ttu-id="f83b8-112">Emplacement du fichier de définition du caractère spécifié dans le fichier local.</span><span class="sxs-lookup"><span data-stu-id="f83b8-112">The local file location of the specified character's definition file.</span></span> |
| <span data-ttu-id="f83b8-113">*URL*</span><span class="sxs-lookup"><span data-stu-id="f83b8-113">*URL*</span></span>      | <span data-ttu-id="f83b8-114">Adresse HTTP du fichier de définition du caractère.</span><span class="sxs-lookup"><span data-stu-id="f83b8-114">The HTTP address for the character's definition file.</span></span>                 |



 

</dd> <dt>

<span data-ttu-id="f83b8-115"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*</span><span class="sxs-lookup"><span data-stu-id="f83b8-115"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="f83b8-116">Adresse d’une variable qui reçoit l’ID du caractère.</span><span class="sxs-lookup"><span data-stu-id="f83b8-116">Address of a variable that receives the character's ID.</span></span>

</dd> <dt>

<span data-ttu-id="f83b8-117"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="f83b8-117"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="f83b8-118">Adresse d’une variable qui reçoit l’ID de la demande de [**chargement**](load-method.md) .</span><span class="sxs-lookup"><span data-stu-id="f83b8-118">Address of a variable that receives the [**Load**](load-method.md) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="f83b8-119">Vous pouvez charger des caractères à partir du sous-répertoire Microsoft Agent en spécifiant un chemin d’accès relatif (un caractère qui n’inclut pas de deux-points ou d’une barre oblique de début).</span><span class="sxs-lookup"><span data-stu-id="f83b8-119">You can load characters from the Microsoft Agent subdirectory by specifying a relative path (one that does not include a colon or leading slash character).</span></span> <span data-ttu-id="f83b8-120">Cela préfixe le chemin d’accès avec le répertoire de caractères de l’agent (situé dans le répertoire% Windows% \\ msagent localisé).</span><span class="sxs-lookup"><span data-stu-id="f83b8-120">This prefixes the path with Agent's characters directory (located in the localized %windows%\\msagent directory).</span></span> <span data-ttu-id="f83b8-121">Vous pouvez également utiliser une adresse relative pour spécifier votre propre répertoire dans le répertoire de caractères de l’agent.</span><span class="sxs-lookup"><span data-stu-id="f83b8-121">You can also use a relative address to specify your own directory in Agent's Chars directory.</span></span>

<span data-ttu-id="f83b8-122">Vous ne pouvez pas charger le même caractère (un caractère ayant le même GUID) plusieurs fois à partir d’une seule connexion.</span><span class="sxs-lookup"><span data-stu-id="f83b8-122">You cannot load the same character (a character having the same GUID) more than once from a single connection.</span></span> <span data-ttu-id="f83b8-123">De même, vous ne pouvez pas charger le caractère par défaut et d’autres caractères en même temps à partir d’une seule connexion, car le caractère par défaut peut être identique à l’autre caractère.</span><span class="sxs-lookup"><span data-stu-id="f83b8-123">Similarly, you cannot load the default character and other characters at the same time from a single connection, because the default character could be the same as the other character.</span></span> <span data-ttu-id="f83b8-124">Toutefois, vous pouvez créer une autre connexion (à l’aide de CoCreateInstance) et charger le même caractère.</span><span class="sxs-lookup"><span data-stu-id="f83b8-124">However, you can create another connection (using CoCreateInstance) and load the same character.</span></span>

<span data-ttu-id="f83b8-125">Le fournisseur de données de Microsoft agent prend en charge le chargement de données de caractères stockées sous la forme d’un fichier structuré unique (. ACS) avec les données de caractères et les données d’animation ensemble, ou en tant que données de caractères distinctes (. ACF) et d’animation (. ).</span><span class="sxs-lookup"><span data-stu-id="f83b8-125">Microsoft Agent's data provider supports loading character data stored as a single structured file (.ACS) with character data and animation data together, or as separate character data (.ACF) and animation (.ACA) files.</span></span> <span data-ttu-id="f83b8-126">En règle générale, utilisez la structure structurée unique. Fichier ACS pour charger un caractère stocké sur un lecteur de disque local ou un réseau et accessible à l’aide du protocole de fichier conventionnel (tel que les chemins d’accès UNC).</span><span class="sxs-lookup"><span data-stu-id="f83b8-126">Generally, use the single structured .ACS file to load a character that is stored on a local disk drive or network and accessed using conventional file protocol (such as UNC pathnames).</span></span> <span data-ttu-id="f83b8-127">Utilisez le distinct. ACF et. Les fichiers de CCN lorsque vous souhaitez charger les fichiers d’animation individuellement à partir d’un site distant où ils sont accessibles via le protocole HTTP.</span><span class="sxs-lookup"><span data-stu-id="f83b8-127">Use the separate .ACF and .ACA files when you want to load the animation files individually from a remote site where they are accessed using HTTP protocol.</span></span>

<span data-ttu-id="f83b8-128">Pour. Les fichiers ACS, à l’aide de la méthode [**Load**](load-method.md) , permettent d’accéder aux animations d’un caractère. une fois chargé, vous pouvez utiliser la méthode [**Play**](play-method.md) pour animer le caractère.</span><span class="sxs-lookup"><span data-stu-id="f83b8-128">For .ACS files, using the [**Load**](load-method.md) method provides access a character's animations; once loaded, you can use the [**Play**](play-method.md) method to animate the character.</span></span> <span data-ttu-id="f83b8-129">Pour. Fichiers ACF, vous utilisez également la méthode [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) pour charger les données d’animation.</span><span class="sxs-lookup"><span data-stu-id="f83b8-129">For .ACF files, you also use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to load animation data.</span></span> <span data-ttu-id="f83b8-130">La méthode **Load** ne prend pas en charge le téléchargement. Fichiers ACS à partir d’un site HTTP.</span><span class="sxs-lookup"><span data-stu-id="f83b8-130">The **Load** method does not support downloading .ACS files from an HTTP site.</span></span>

<span data-ttu-id="f83b8-131">Le chargement d’un caractère n’affiche pas automatiquement le caractère.</span><span class="sxs-lookup"><span data-stu-id="f83b8-131">Loading a character does not automatically display the character.</span></span> <span data-ttu-id="f83b8-132">Utilisez d’abord la méthode [**Show**](show-method.md) pour rendre le caractère visible.</span><span class="sxs-lookup"><span data-stu-id="f83b8-132">Use the [**Show**](show-method.md) method first to make the character visible.</span></span>

 

 