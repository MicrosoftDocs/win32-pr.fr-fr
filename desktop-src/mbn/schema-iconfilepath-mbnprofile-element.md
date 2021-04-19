---
description: Contient le chemin d’accès du fichier d’icône pour la connexion.
ms.assetid: 9daf4916-914b-4326-9933-b433cc00b4c1
title: Élément ICONFilePath (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICONFilePath
api_type:
- Schema
ms.openlocfilehash: 6b1e98f76fe2f83ce214076223b5a1439bd0ea45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517287"
---
# <a name="iconfilepath-mbnprofile-element"></a><span data-ttu-id="d8fc3-103">Élément ICONFilePath (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="d8fc3-103">ICONFilePath (MBNProfile) Element</span></span>

<span data-ttu-id="d8fc3-104">L’élément **ICONFilePath (MBNProfile)** contient le chemin d’accès du fichier d’icône pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="d8fc3-104">The **ICONFilePath (MBNProfile)** element contains the path of the icon file for the connection.</span></span>

<span data-ttu-id="d8fc3-105">L’interface utilisateur de connexion du système d’exploitation affiche cette icône lorsqu’une connexion est établie à l’aide de cet élément.</span><span class="sxs-lookup"><span data-stu-id="d8fc3-105">The operating system connection UI will display this icon when a connection is made using this element.</span></span>

<span data-ttu-id="d8fc3-106">Lorsque vous passez le XML pour créer le profil dans la méthode [**CreateConnectionProfile**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile) de l’interface [**IMbnConnectionProfileManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager) , ce chemin d’accès doit pointer vers l’emplacement source du fichier d’icône.</span><span class="sxs-lookup"><span data-stu-id="d8fc3-106">When passing the XML for creating the profile in the [**CreateConnectionProfile**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile) method of the [**IMbnConnectionProfileManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager) interface, this path should point to the source location of the icon file.</span></span> <span data-ttu-id="d8fc3-107">En cas de réussite de la création de l’objet [**IMbnConnectionProfile**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) , le service haut débit mobile copie le fichier d’icône dans son magasin interne et le chemin du profil est modifié pour en tenir compte.</span><span class="sxs-lookup"><span data-stu-id="d8fc3-107">On successful creation of [**IMbnConnectionProfile**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) object, the Mobile Broadband service will copy the icon file in it's internal store and the profile path will be modified to reflect this.</span></span>

<span data-ttu-id="d8fc3-108">Le fichier d’icône doit être au format. bmp avec une dimension de pixels de 32X32.</span><span class="sxs-lookup"><span data-stu-id="d8fc3-108">The icon file should be in .bmp format with 32X32 pixel dimension.</span></span>

<span data-ttu-id="d8fc3-109">Cet élément est une chaîne d’une longueur maximale de 1024 caractères, contenant un chemin d’accès absolu au fichier.</span><span class="sxs-lookup"><span data-stu-id="d8fc3-109">This element is a string of length up to 1024 characters, containing an absolute file path.</span></span>

<span data-ttu-id="d8fc3-110">L’élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="d8fc3-110">The element is optional.</span></span>

``` syntax
<xs:element name="ICONFilePath"
    type="iconFileType"
 />
```

<span data-ttu-id="d8fc3-111">L’élément **ICONFilePath** est défini par l’élément [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d8fc3-111">The **ICONFilePath** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8fc3-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8fc3-112">Requirements</span></span>



| <span data-ttu-id="d8fc3-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8fc3-113">Requirement</span></span> | <span data-ttu-id="d8fc3-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8fc3-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="d8fc3-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8fc3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d8fc3-116">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d8fc3-116">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="d8fc3-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8fc3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d8fc3-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8fc3-118">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="d8fc3-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8fc3-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="d8fc3-120">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="d8fc3-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d8fc3-121">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="d8fc3-121">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="d8fc3-122">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="d8fc3-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d8fc3-123">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="d8fc3-123">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




