---
title: IWMPSettings, propriété baseURL
description: La propriété baseURL obtient ou définit l’URL de base utilisée pour la résolution de chemin d’accès relative avec des commandes de script d’URL incorporées dans le contenu multimédia numérique.
ms.assetid: e136303f-ba08-434f-ad7e-9fffa66785c4
keywords:
- propriété baseURL lecteur Windows Media
- propriété baseURL lecteur Windows Media, interface IWMPSettings
- Interface IWMPSettings lecteur Windows Media, propriété baseURL
topic_type:
- apiref
api_name:
- IWMPSettings.baseURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 393575a93bf904f6fe312b13647ad5a7557b15bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528607"
---
# <a name="iwmpsettingsbaseurl-property"></a><span data-ttu-id="d77e2-106">IWMPSettings :: baseURL, propriété</span><span class="sxs-lookup"><span data-stu-id="d77e2-106">IWMPSettings::baseURL property</span></span>

<span data-ttu-id="d77e2-107">La propriété **baseURL** obtient ou définit l’URL de base utilisée pour la résolution de chemin d’accès relative avec des commandes de script d’URL incorporées dans le contenu multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="d77e2-107">The **baseURL** property gets or sets the base URL used for relative path resolution with URL script commands that are embedded in digital media content.</span></span>

## <a name="syntax"></a><span data-ttu-id="d77e2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d77e2-108">Syntax</span></span>


```CSharp
public System.String baseURL {get; set;}
```


```VB

Public Property baseURL As System.String
```





## <a name="property-value"></a><span data-ttu-id="d77e2-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d77e2-109">Property value</span></span>

<span data-ttu-id="d77e2-110">**System. String** qui est l’URL de base.</span><span class="sxs-lookup"><span data-stu-id="d77e2-110">A **System.String** that is the base URL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d77e2-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d77e2-111">Remarks</span></span>

<span data-ttu-id="d77e2-112">Cette propriété spécifie l’URL HTTP de base qui est transmise en tant que paramètre de commande par l’événement **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** .</span><span class="sxs-lookup"><span data-stu-id="d77e2-112">This property specifies the base HTTP URL that is passed as the command parameter by the **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event.</span></span> <span data-ttu-id="d77e2-113">L’URL de base est concaténée avec l’URL relative, comme suit :</span><span class="sxs-lookup"><span data-stu-id="d77e2-113">The base URL is concatenated with the relative URL as follows:</span></span>

1.  <span data-ttu-id="d77e2-114">Une barre oblique finale (/) est ajoutée à la valeur récupérée par la propriété **baseURL** .</span><span class="sxs-lookup"><span data-stu-id="d77e2-114">A trailing forward slash (/) is added to the value retrieved by the **baseURL** property.</span></span>
2.  <span data-ttu-id="d77e2-115">Un point de début, une barre oblique inverse ou un caractère de barre oblique (., \\ et/) est supprimé de l’URL relative.</span><span class="sxs-lookup"><span data-stu-id="d77e2-115">A leading period, backward slash, or forward slash character (., \\, and /) is deleted from the relative URL.</span></span>
3.  <span data-ttu-id="d77e2-116">L’URL relative est ajoutée à la fin de l’URL de base.</span><span class="sxs-lookup"><span data-stu-id="d77e2-116">The relative URL is added to the end of the base URL.</span></span>
4.  <span data-ttu-id="d77e2-117">Tous les caractères de barre oblique dans l’URL complète résultante sont pointés dans la même direction (convertis en barres obliques ou en arrière) en fonction de la direction de la première barre oblique rencontrée dans la nouvelle URL.</span><span class="sxs-lookup"><span data-stu-id="d77e2-117">All slash characters in the resulting fully qualified URL are pointed in the same direction (converted to forward or backward slashes) based on the direction of the first slash character encountered in the new URL.</span></span>

<span data-ttu-id="d77e2-118">**Remarque**</span><span class="sxs-lookup"><span data-stu-id="d77e2-118">**Note**</span></span>

<span data-ttu-id="d77e2-119">Le contrôle du lecteur Windows Media ne prend pas en charge l’utilisation de deux points (..) dans l’URL relative pour indiquer le parent de l’emplacement actuel.</span><span class="sxs-lookup"><span data-stu-id="d77e2-119">The Windows Media Player control does not support the use of two periods (..) in the relative URL to indicate the parent of the current location.</span></span>

## <a name="requirements"></a><span data-ttu-id="d77e2-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d77e2-120">Requirements</span></span>



| <span data-ttu-id="d77e2-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d77e2-121">Requirement</span></span> | <span data-ttu-id="d77e2-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="d77e2-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d77e2-123">Version</span><span class="sxs-lookup"><span data-stu-id="d77e2-123">Version</span></span><br/>   | <span data-ttu-id="d77e2-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="d77e2-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d77e2-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d77e2-125">Namespace</span></span><br/> | <span data-ttu-id="d77e2-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d77e2-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d77e2-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="d77e2-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d77e2-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d77e2-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d77e2-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d77e2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d77e2-130">**Événement AxWindowsMediaPlayer. commande (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d77e2-130">**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="d77e2-131">**Interface IWMPSettings (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d77e2-131">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





