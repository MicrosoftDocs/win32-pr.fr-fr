---
description: Les fonctions de boîte de dialogue spécifiques au fournisseur permettent à un fournisseur d’afficher et de gérer des informations spécifiques au réseau en modifiant des boîtes de dialogue système ou en affichant des boîtes de dialogue personnalisées.
ms.assetid: c9a52867-0a0b-40d8-a09d-2b7bed517e13
title: Provider-Specific les fonctions de boîte de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 567c4dcb9f1fd6c2e289d678cf09b3d0d66e4207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536400"
---
# <a name="provider-specific-dialog-box-functions"></a><span data-ttu-id="a2b0e-103">Provider-Specific les fonctions de boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="a2b0e-103">Provider-Specific Dialog Box Functions</span></span>

<span data-ttu-id="a2b0e-104">Les fonctions de boîte de dialogue spécifiques au fournisseur permettent à un fournisseur d’afficher et de gérer des informations spécifiques au réseau en modifiant des boîtes de dialogue système ou en affichant des boîtes de dialogue personnalisées.</span><span class="sxs-lookup"><span data-stu-id="a2b0e-104">Provider-specific dialog box functions enable a provider to display and handle network-specific information by altering system dialog boxes or displaying custom dialog boxes.</span></span>

<span data-ttu-id="a2b0e-105">Les fonctions de boîte de dialogue suivantes ajoutent des boutons à la boîte de dialogue **Propriétés** du gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="a2b0e-105">The following dialog box functions add buttons to the File Manager **Properties** dialog box.</span></span> <span data-ttu-id="a2b0e-106">Le fournisseur peut ensuite gérer les événements de ces boutons pour effectuer des tâches spécifiques au réseau.</span><span class="sxs-lookup"><span data-stu-id="a2b0e-106">The provider can then handle the events of those buttons to perform network-specific tasks.</span></span> <span data-ttu-id="a2b0e-107">Notez qu’il existe une limite au nombre de boutons qui peuvent être ajoutés.</span><span class="sxs-lookup"><span data-stu-id="a2b0e-107">Note that there is a limit to the number of buttons that can be added.</span></span> <span data-ttu-id="a2b0e-108">Pour cette raison, les fournisseurs doivent utiliser cette fonctionnalité avec modération.</span><span class="sxs-lookup"><span data-stu-id="a2b0e-108">Because of this, providers should use this capability sparingly.</span></span> <span data-ttu-id="a2b0e-109">En outre, un fournisseur peut ne pas être en mesure d’ajouter un bouton, car l’espace disponible a déjà été utilisé par d’autres fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="a2b0e-109">Also, a provider may find itself unable to add a button because the available space has been used already by other providers.</span></span> <span data-ttu-id="a2b0e-110">Un fournisseur de réseau doit gérer cette situation.</span><span class="sxs-lookup"><span data-stu-id="a2b0e-110">A network provider should handle this situation.</span></span>



| <span data-ttu-id="a2b0e-111">Fonction</span><span class="sxs-lookup"><span data-stu-id="a2b0e-111">Function</span></span>                                           | <span data-ttu-id="a2b0e-112">Description</span><span class="sxs-lookup"><span data-stu-id="a2b0e-112">Description</span></span>                                                                                                                             |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2b0e-113">**NPGetPropertyText**</span><span class="sxs-lookup"><span data-stu-id="a2b0e-113">**NPGetPropertyText**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext)     | <span data-ttu-id="a2b0e-114">Détermine les noms des boutons ajoutés à une boîte de dialogue de propriétés pour une ressource spécifique.</span><span class="sxs-lookup"><span data-stu-id="a2b0e-114">Determines the names of buttons added to a property dialog box for a specific resource.</span></span><br/>                                      |
| [<span data-ttu-id="a2b0e-115">**NPPropertyDialog**</span><span class="sxs-lookup"><span data-stu-id="a2b0e-115">**NPPropertyDialog**</span></span>](/windows/desktop/api/Npapi/nf-npapi-nppropertydialog)       | <span data-ttu-id="a2b0e-116">Appelée lorsqu’un utilisateur clique sur un bouton ajouté à l’aide de la fonction [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext) .</span><span class="sxs-lookup"><span data-stu-id="a2b0e-116">Called when a user clicks a button added by using the [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext) function.</span></span><br/>               |
| [<span data-ttu-id="a2b0e-117">**NPSearchDialog**</span><span class="sxs-lookup"><span data-stu-id="a2b0e-117">**NPSearchDialog**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npsearchdialog)           | <span data-ttu-id="a2b0e-118">Permet aux fournisseurs réseau d’implémenter leur propre fonctionnalité de recherche au-delà de celle fournie dans la boîte de dialogue de **connexion** .</span><span class="sxs-lookup"><span data-stu-id="a2b0e-118">Enables network providers to implement their own search functionality beyond that provided in the **Connection** dialog box.</span></span><br/> |
| [<span data-ttu-id="a2b0e-119">**NPFormatNetworkName**</span><span class="sxs-lookup"><span data-stu-id="a2b0e-119">**NPFormatNetworkName**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npformatnetworkname) | <span data-ttu-id="a2b0e-120">Permet aux fournisseurs de réseau de mettre en forme ou de modifier des noms réseau avant qu’ils ne soient présentés à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a2b0e-120">Enables network providers to format or otherwise modify network names before they are presented to the user.</span></span><br/>                 |



 

 

 




