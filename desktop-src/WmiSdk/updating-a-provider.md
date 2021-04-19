---
description: Parfois, vous devrez peut-être installer une version plus récente d’un fournisseur sur un système en cours d’exécution.
ms.assetid: 44c4c16a-fd79-483a-81ef-a0f74a2cdf45
ms.tgt_platform: multiple
title: Mise à jour d’un fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4869e6e9f7fbddc3081922f476ca021934065a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530883"
---
# <a name="updating-a-provider"></a><span data-ttu-id="3406d-103">Mise à jour d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="3406d-103">Updating a Provider</span></span>

<span data-ttu-id="3406d-104">Parfois, vous devrez peut-être installer une version plus récente d’un fournisseur sur un système en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="3406d-104">Sometimes you may need to install a newer version of a provider onto a running system.</span></span> <span data-ttu-id="3406d-105">Si votre fournisseur est installé en tant que DLL, vous pouvez installer un nouveau fournisseur sans avoir à redémarrer le service, redémarrer l’ordinateur ou affecter une autre application à l’aide de WMI à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="3406d-105">If your provider is installed as a DLL, you can install a new provider without having to restart the service, reboot the computer, or otherwise affect any applications using WMI at that time.</span></span>

<span data-ttu-id="3406d-106">La procédure suivante décrit comment mettre à jour un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3406d-106">The following procedure describes how to update a provider.</span></span>

<span data-ttu-id="3406d-107">**Pour mettre à jour un fournisseur**</span><span class="sxs-lookup"><span data-stu-id="3406d-107">**To update a provider**</span></span>

1.  <span data-ttu-id="3406d-108">Générez le nouveau fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3406d-108">Build the new provider.</span></span>

    1.  <span data-ttu-id="3406d-109">Compilez le nouveau fournisseur avec un nom de DLL et un **CLSID** différents.</span><span class="sxs-lookup"><span data-stu-id="3406d-109">Compile the new provider with a different DLL name and a different **CLSID**.</span></span>

        <span data-ttu-id="3406d-110">Par exemple, remplacez Myprov.dll par Myprov1.dll et **CLSID \_ MyProProv** par **CLSID \_ MyProv** 1.</span><span class="sxs-lookup"><span data-stu-id="3406d-110">For example, change Myprov.dll to Myprov1.dll, and **CLSID\_MyProProv** to **CLSID\_MyProv** 1.</span></span>

    2.  <span data-ttu-id="3406d-111">Modifiez le fichier MOF d’inscription du fournisseur pour utiliser le nouveau CLSID (CLSID \_ MyProv1), mais le même nom de fournisseur (« MyProv »).</span><span class="sxs-lookup"><span data-stu-id="3406d-111">Modify the provider registration MOF file to use the new CLSID (CLSID\_MyProv1), but the same provider name ("MyProv").</span></span>

2.  <span data-ttu-id="3406d-112">Installez le nouveau fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3406d-112">Install the new provider.</span></span>

    1.  <span data-ttu-id="3406d-113">Copiez la nouvelle DLL du fournisseur avec le nouveau nom en regard de l’ancien.</span><span class="sxs-lookup"><span data-stu-id="3406d-113">Copy the new provider DLL with the new name alongside the old one.</span></span>
    2.  <span data-ttu-id="3406d-114">Inscrire automatiquement le nouveau fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3406d-114">Self-register the new provider.</span></span>

        <span data-ttu-id="3406d-115">Par exemple, utilisez la commande **regsvr32** **myprov1.dll** pour inscrire le nouveau fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3406d-115">For example, use the **regsvr32** **myprov1.dll** command to register the new provider.</span></span>

    3.  <span data-ttu-id="3406d-116">Compilez le nouveau MOF d’inscription du fournisseur, remplaçant ainsi l’ancien enregistrement du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3406d-116">Compile the new provider registration MOF, thus overwriting the old provider registration.</span></span> <span data-ttu-id="3406d-117">Jusqu’à ce stade, l’ancien fournisseur était entièrement opérationnel ; désormais, le nouveau fournisseur est entièrement opérationnel.</span><span class="sxs-lookup"><span data-stu-id="3406d-117">Until this point, the old provider was fully functional; now the new provider is fully operational.</span></span>

3.  <span data-ttu-id="3406d-118">Supprimez l’ancienne version du fournisseur, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3406d-118">Remove the old version of the provider, if necessary.</span></span>

    1.  <span data-ttu-id="3406d-119">Annulez l’inscription de l’ancienne DLL.</span><span class="sxs-lookup"><span data-stu-id="3406d-119">Unregister the old DLL.</span></span>

        <span data-ttu-id="3406d-120">Par exemple, utilisez la commande **regsvr32** **/umyprov.dll** pour annuler l’inscription de l’ancienne dll.</span><span class="sxs-lookup"><span data-stu-id="3406d-120">For example, use the **regsvr32** **/umyprov.dll** command to unregister the old DLL.</span></span>

    2.  <span data-ttu-id="3406d-121">Marquez l’ancienne DLL à supprimer lors du redémarrage en appelant [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa).</span><span class="sxs-lookup"><span data-stu-id="3406d-121">Mark the old DLL to be deleted on reboot by calling [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa).</span></span>

<span data-ttu-id="3406d-122">Vous pouvez prendre des mesures similaires pour mettre à niveau un fournisseur local implémenté par le serveur.</span><span class="sxs-lookup"><span data-stu-id="3406d-122">You can take similar steps to upgrade a local server-implemented provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3406d-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3406d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3406d-124">Développement d’un fournisseur WMI</span><span class="sxs-lookup"><span data-stu-id="3406d-124">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="3406d-125">Définition des descripteurs de sécurité espace</span><span class="sxs-lookup"><span data-stu-id="3406d-125">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="3406d-126">Sécurisation de votre fournisseur</span><span class="sxs-lookup"><span data-stu-id="3406d-126">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 
