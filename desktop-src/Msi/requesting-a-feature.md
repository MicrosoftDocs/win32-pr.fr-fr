---
description: Il existe plusieurs fonctions qu’une application doit appeler pour demander des fonctionnalités.
ms.assetid: 5253c6f0-316f-4f24-b0c0-951db8d16745
title: Demande d’une fonctionnalité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5261aac69ad2dd604a072e4b02e3bcde76a2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034748"
---
# <a name="requesting-a-feature"></a><span data-ttu-id="1a5c9-103">Demande d’une fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="1a5c9-103">Requesting a Feature</span></span>

<span data-ttu-id="1a5c9-104">Il existe plusieurs fonctions qu’une application doit appeler pour demander des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="1a5c9-104">There are several functions an application must call to request features.</span></span> <span data-ttu-id="1a5c9-105">Avant de demander une fonctionnalité, l’application doit s’assurer que la fonctionnalité est installée.</span><span class="sxs-lookup"><span data-stu-id="1a5c9-105">Before requesting a feature, the application must ensure that the feature is installed.</span></span> <span data-ttu-id="1a5c9-106">Si l’application appelle [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) avant que l’application n’accède à une fonctionnalité, l’application peut utiliser les informations retournées pour conserver les métriques d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="1a5c9-106">If the application calls [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) before the application accesses a feature, the application can use the information returned to maintain usage metrics.</span></span>

<span data-ttu-id="1a5c9-107">**Pour demander une fonctionnalité**</span><span class="sxs-lookup"><span data-stu-id="1a5c9-107">**To request a feature**</span></span>

1.  <span data-ttu-id="1a5c9-108">Appelez la fonction [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) ou [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) si vous souhaitez déterminer la disponibilité d’une fonctionnalité sans incrémenter le nombre d’utilisations.</span><span class="sxs-lookup"><span data-stu-id="1a5c9-108">Call the [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) or the [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) function if you want to determine the availability of a feature without incrementing the usage count.</span></span>
2.  <span data-ttu-id="1a5c9-109">Indiquez l’intention de votre application d’utiliser une fonctionnalité en appelant la fonction [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) .</span><span class="sxs-lookup"><span data-stu-id="1a5c9-109">Indicate your application's intent to use a feature by calling the [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) function.</span></span>
3.  <span data-ttu-id="1a5c9-110">Déterminez les emplacements des fichiers en appelant la fonction [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) .</span><span class="sxs-lookup"><span data-stu-id="1a5c9-110">Determine file locations by calling the [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) function.</span></span>
4.  <span data-ttu-id="1a5c9-111">Configurez la fonctionnalité en appelant la fonction [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) .</span><span class="sxs-lookup"><span data-stu-id="1a5c9-111">Configure the feature by calling the [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) function.</span></span>
5.  <span data-ttu-id="1a5c9-112">Obtenez les métriques d’utilisation que votre application peut utiliser en appelant la fonction [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) .</span><span class="sxs-lookup"><span data-stu-id="1a5c9-112">Obtain usage metrics that your application can use by calling the [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) function.</span></span>

<span data-ttu-id="1a5c9-113">Le diagramme suivant illustre le modèle de demande de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="1a5c9-113">The following diagram illustrates the feature request model.</span></span>

![<span data-ttu-id="1a5c9-114">modèle de demande de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="1a5c9-114">feature request model.</span></span> ](images/over2.png)

 

 



