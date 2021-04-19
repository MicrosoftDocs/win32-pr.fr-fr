---
title: Méthode DownloadCollection. startDownload
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La méthode startDownload met en file d’attente un téléchargement.
ms.assetid: 54cf91fe-cef9-4424-9f99-629e773eade1
keywords:
- méthode startDownload lecteur Windows Media
- méthode startDownload lecteur Windows Media, classe DownloadCollection
- Classe DownloadCollection lecteur Windows Media, méthode startDownload
topic_type:
- apiref
api_name:
- DownloadCollection.startDownload
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3187ce00dda45f7e4660b4961c78af6db2af50e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528955"
---
# <a name="downloadcollectionstartdownload-method"></a><span data-ttu-id="dac31-108">Méthode DownloadCollection. startDownload</span><span class="sxs-lookup"><span data-stu-id="dac31-108">DownloadCollection.startDownload method</span></span>

> [!Note]  
> <span data-ttu-id="dac31-109">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="dac31-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="dac31-110">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="dac31-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="dac31-111">La méthode **startDownload** met en file d’attente un téléchargement.</span><span class="sxs-lookup"><span data-stu-id="dac31-111">The **startDownload** method queues a download.</span></span>

## <a name="syntax"></a><span data-ttu-id="dac31-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dac31-112">Syntax</span></span>


```JScript
retVal = DownloadCollection.startDownload(
  sourceURL,
  type
)
```



## <a name="parameters"></a><span data-ttu-id="dac31-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dac31-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dac31-114">*sourceURL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dac31-114">*sourceURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dac31-115">**Chaîne** spécifiant l’URL du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="dac31-115">**String** specifying the URL of the download.</span></span>

</dd> <dt>

<span data-ttu-id="dac31-116">*type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dac31-116">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dac31-117">**Chaîne** spécifiant le type de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="dac31-117">**String** specifying the type of download.</span></span> <span data-ttu-id="dac31-118">Contient l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="dac31-118">Contains one of the following values.</span></span>



| <span data-ttu-id="dac31-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="dac31-119">Value</span></span>      | <span data-ttu-id="dac31-120">Description</span><span class="sxs-lookup"><span data-stu-id="dac31-120">Description</span></span>                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dac31-121">background</span><span class="sxs-lookup"><span data-stu-id="dac31-121">background</span></span> | <span data-ttu-id="dac31-122">(Windows XP et versions ultérieures.) Le téléchargement se produit en tant que processus en arrière-plan, car le temps processeur devient disponible.</span><span class="sxs-lookup"><span data-stu-id="dac31-122">(Windows XP and later.) The download occurs as a background process as processor time becomes available.</span></span> <span data-ttu-id="dac31-123">Les États de téléchargement persistent même lorsque Windows Media Player ou Windows XP est arrêté.</span><span class="sxs-lookup"><span data-stu-id="dac31-123">Download states persist even when Windows Media Player or Windows XP is shut down.</span></span> |
| <span data-ttu-id="dac31-124">temps réel</span><span class="sxs-lookup"><span data-stu-id="dac31-124">real time</span></span>  | <span data-ttu-id="dac31-125">(Tous les systèmes d’exploitation pris en charge.) Le téléchargement a lieu en même temps.</span><span class="sxs-lookup"><span data-stu-id="dac31-125">(All supported operating systems.) The download occurs all at once.</span></span> <span data-ttu-id="dac31-126">Aucun État de téléchargement n’est conservé entre les sessions.</span><span class="sxs-lookup"><span data-stu-id="dac31-126">No download states persist between sessions.</span></span>                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dac31-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dac31-127">Return value</span></span>

<span data-ttu-id="dac31-128">Cette méthode retourne un objet **DownloadItem** .</span><span class="sxs-lookup"><span data-stu-id="dac31-128">This method returns a **DownloadItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dac31-129">Notes</span><span class="sxs-lookup"><span data-stu-id="dac31-129">Remarks</span></span>

<span data-ttu-id="dac31-130">Lors du démarrage d’un nouveau téléchargement, le gestionnaire de téléchargement l’ajoute en tant qu’élément à la collection de téléchargements qui a initié le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="dac31-130">When a new download is started, Download Manager adds it as an item to the download collection that initiated the download.</span></span>

<span data-ttu-id="dac31-131">Seuls les formats multimédias numériques suivants peuvent être téléchargés :</span><span class="sxs-lookup"><span data-stu-id="dac31-131">Only the following digital media formats can be downloaded:</span></span>

-   <span data-ttu-id="dac31-132">ASF (Advanced Systems Format)</span><span class="sxs-lookup"><span data-stu-id="dac31-132">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="dac31-133">MP3</span><span class="sxs-lookup"><span data-stu-id="dac31-133">MP3</span></span>
-   <span data-ttu-id="dac31-134">Audio Windows Media (WMA)</span><span class="sxs-lookup"><span data-stu-id="dac31-134">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="dac31-135">Vidéo Windows Media (WMV)</span><span class="sxs-lookup"><span data-stu-id="dac31-135">Windows Media Video (WMV)</span></span>

<span data-ttu-id="dac31-136">Le paramètre *sourceURL* ne prend pas en charge les chaînes encodées en Unicode.</span><span class="sxs-lookup"><span data-stu-id="dac31-136">The *sourceURL* parameter does not support Unicode-encoded strings.</span></span> <span data-ttu-id="dac31-137">Il doit pointer vers un contenu valide.</span><span class="sxs-lookup"><span data-stu-id="dac31-137">It must point to valid content.</span></span> <span data-ttu-id="dac31-138">Les redirections ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="dac31-138">Redirects are not supported.</span></span>

<span data-ttu-id="dac31-139">Lorsque vous utilisez Windows XP, les fichiers audio sont automatiquement placés dans mes sous-dossiers de **musique** appropriés en fonction des valeurs de métadonnées au niveau du fichier.</span><span class="sxs-lookup"><span data-stu-id="dac31-139">When using Windows XP, audio files are automatically placed into appropriate **My Music** subfolders based upon file-level metadata values.</span></span> <span data-ttu-id="dac31-140">Les fichiers vidéo sont placés dans \\ \\ \\ le type de *nombre aléatoire* à télécharger musique \\ , où *nombre aléatoire* est une valeur aléatoire générée par le lecteur Windows Media pour chaque utilisateur, et le *type* est soit « temps réel », soit « arrière-plan », selon le type de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="dac31-140">Video files are placed into \\My Music\\download\\*random number*\\*type*, where *random number* is a random value generated by Windows Media Player for each user, and *type* is either "real time" or "background", depending upon the download type.</span></span>

<span data-ttu-id="dac31-141">Lorsque vous utilisez le lecteur Windows Media série 9 avec Windows 98 et Windows Millennium Edition (me), les fichiers audio et vidéo sont placés dans \\ \\ \\  \\ le *type* de nombre aléatoire de musique Download, où le *nombre aléatoire* est une valeur aléatoire générée par le joueur pour chaque utilisateur, et le *type* est « temps réel » ou « arrière-plan », selon le type de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="dac31-141">When using Windows Media Player 9 Series with Windows 98 and Windows Millennium Edition (ME), audio and video files are placed into \\My Music\\download\\*random number*\\*type*, where *random number* is a random value generated by the Player for each user, and *type* is either "real time" or "background", depending upon the download type.</span></span>

<span data-ttu-id="dac31-142">Notez que les fichiers peuvent être renommés en fonction des attributs de métadonnées contenus dans le fichier et des règles spécifiés par l’utilisateur dans la boîte de dialogue **options** .</span><span class="sxs-lookup"><span data-stu-id="dac31-142">Note that files may be renamed based upon metadata attributes contained in the file and rules specified by the user in the **Options** dialog box.</span></span> <span data-ttu-id="dac31-143">Les fichiers qui ne contiennent pas de métadonnées, tels que des **albums** ou des **artistes**, peuvent être déplacés vers des dossiers intitulés artiste inconnu ou album inconnu.</span><span class="sxs-lookup"><span data-stu-id="dac31-143">Files that don't contain metadata, such as **Album** or **Artist**, may be moved to folders labeled Unknown Artist or Unknown Album.</span></span>

## <a name="requirements"></a><span data-ttu-id="dac31-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dac31-144">Requirements</span></span>



| <span data-ttu-id="dac31-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dac31-145">Requirement</span></span> | <span data-ttu-id="dac31-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="dac31-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dac31-147">Version</span><span class="sxs-lookup"><span data-stu-id="dac31-147">Version</span></span><br/> | <span data-ttu-id="dac31-148">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="dac31-148">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="dac31-149">DLL</span><span class="sxs-lookup"><span data-stu-id="dac31-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="dac31-150"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dac31-150"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dac31-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dac31-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dac31-152">**Objet DownloadCollection**</span><span class="sxs-lookup"><span data-stu-id="dac31-152">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> <dt>

[<span data-ttu-id="dac31-153">**Objet DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="dac31-153">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





