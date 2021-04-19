---
title: Méthode AxWindowsMediaPlayer. newPlaylist
description: La méthode newPlaylist renvoie une interface IWMPPlaylist pour une nouvelle sélection.
ms.assetid: caee8ee5-6201-474d-a4cb-80e574f84f0b
keywords:
- méthode newPlaylist lecteur Windows Media
- méthode newPlaylist lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, méthode newPlaylist
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8dc82be7aae37b4c1334b79f84e9d607b4f73cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543833"
---
# <a name="axwindowsmediaplayernewplaylist-method"></a><span data-ttu-id="16595-106">Méthode AxWindowsMediaPlayer. newPlaylist</span><span class="sxs-lookup"><span data-stu-id="16595-106">AxWindowsMediaPlayer.newPlaylist method</span></span>

<span data-ttu-id="16595-107">La méthode newPlaylist renvoie une interface IWMPPlaylist pour une nouvelle sélection.</span><span class="sxs-lookup"><span data-stu-id="16595-107">The newPlaylist method returns an IWMPPlaylist interface for a new playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="16595-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16595-108">Syntax</span></span>


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName,
  System.String bstrURL
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String, _
  ByVal bstrURL As System.String _
) As IWMPPlaylist
```





## <a name="parameters"></a><span data-ttu-id="16595-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16595-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16595-110">*bstrName,*</span><span class="sxs-lookup"><span data-stu-id="16595-110">*bstrName*</span></span> 
</dt> <dd>

<span data-ttu-id="16595-111">**System. String** qui est le nom de la nouvelle sélection.</span><span class="sxs-lookup"><span data-stu-id="16595-111">The **System.String** that is the name of the new playlist.</span></span>

</dd> <dt>

<span data-ttu-id="16595-112">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="16595-112">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="16595-113">**System. String** qui est l’URL de la sélection de métafichiers Windows Media utilisée pour initialiser la nouvelle sélection.</span><span class="sxs-lookup"><span data-stu-id="16595-113">The **System.String** that is the URL of the Windows Media metafile playlist that is used to initialize the new playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16595-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16595-114">Return value</span></span>

<span data-ttu-id="16595-115">Interface WMPLib. IWMPPlaylist qui représente la sélection nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="16595-115">A WMPLib.IWMPPlaylist interface that represents the newly created playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="16595-116">Notes</span><span class="sxs-lookup"><span data-stu-id="16595-116">Remarks</span></span>

<span data-ttu-id="16595-117">Si le paramètre *du bstrURL* est une chaîne null ou de longueur nulle (""), cette méthode crée une **sélection** vide.</span><span class="sxs-lookup"><span data-stu-id="16595-117">If the *bstrURL* parameter is a null or zero-length string (""), this method creates an empty **playlist**.</span></span> <span data-ttu-id="16595-118">Si le paramètre *bstrName* est une chaîne de longueur nulle (""), cette méthode applique le nom du métafichier actuel.</span><span class="sxs-lookup"><span data-stu-id="16595-118">If the *bstrName* parameter is a zero-length string (""), this method applies the current metafile name.</span></span>

<span data-ttu-id="16595-119">La nouvelle playlist créée avec cette méthode n’est pas ajoutée à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="16595-119">The new playlist created with this method is not added to the library.</span></span> <span data-ttu-id="16595-120">Pour ajouter une nouvelle sélection à la bibliothèque, utilisez IWMPPlaylistCollection. **importPlaylist** ou IWMPPlaylistCollection. **newPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="16595-120">To add a new playlist to the library, use IWMPPlaylistCollection.**importPlaylist** or IWMPPlaylistCollection.**newPlaylist**.</span></span> <span data-ttu-id="16595-121">Tout espace de début ou de fin dans le nom de la playlist est automatiquement supprimé lorsqu’il est ajouté à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="16595-121">Any leading or trailing spaces in the playlist name are automatically removed when it is added to the library.</span></span>

<span data-ttu-id="16595-122">Étant donné que la bibliothèque autorise plusieurs sélections portant le même nom, vous souhaiterez peut-être vérifier la présence d’une sélection avec un nom donné avant d’en ajouter une nouvelle.</span><span class="sxs-lookup"><span data-stu-id="16595-122">Because the library allows multiple playlists with the same name, you may want to check for the presence of a playlist with a given name before adding a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="16595-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16595-123">Requirements</span></span>



| <span data-ttu-id="16595-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16595-124">Requirement</span></span> | <span data-ttu-id="16595-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="16595-125">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16595-126">Version</span><span class="sxs-lookup"><span data-stu-id="16595-126">Version</span></span><br/>   | <span data-ttu-id="16595-127">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="16595-127">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="16595-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="16595-128">Namespace</span></span><br/> | <span data-ttu-id="16595-129">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="16595-129">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="16595-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="16595-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="16595-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="16595-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16595-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16595-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16595-133">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="16595-133">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="16595-134">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="16595-134">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="16595-135">**IWMPPlaylistCollection. importPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="16595-135">**IWMPPlaylistCollection.importPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="16595-136">**IWMPPlaylistCollection. newPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="16595-136">**IWMPPlaylistCollection.newPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





