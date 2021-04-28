---
description: Compatibilité DEP/NX
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: Compatibilité DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8b46c9143ee96b8599c10d4c70276d36e20a08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116427"
---
# <a name="depnx-compatibility"></a><span data-ttu-id="ceddd-103">Compatibilité DEP/NX</span><span class="sxs-lookup"><span data-stu-id="ceddd-103">DEP/NX compatibility</span></span>

<span data-ttu-id="ceddd-104">Par défaut, dans Windows Internet Explorer 7, DEP/NX est désactivé pour des raisons de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="ceddd-104">By default, in Windows Internet Explorer 7, DEP/NX is disabled for compatibility reasons.</span></span> <span data-ttu-id="ceddd-105">Plusieurs modules complémentaires populaires ne sont pas compatibles avec DEP/NX et échouent lorsque Windows Internet Explorer les charge avec DEP/NX activé.</span><span class="sxs-lookup"><span data-stu-id="ceddd-105">Several popular add-ons are not compatible with DEP/NX and fail when Windows Internet Explorer loads them with DEP/NX enabled.</span></span>

<span data-ttu-id="ceddd-106">En règle générale, ces modules complémentaires sont générés à l’aide d’une version antérieure de l’infrastructure ATL.</span><span class="sxs-lookup"><span data-stu-id="ceddd-106">Typically, these add-ons are built by using an older version of the ATL framework.</span></span> <span data-ttu-id="ceddd-107">ATL 7,1 et les versions antérieures ne sont pas conçus avec la fonctionnalité de sécurité DEP.</span><span class="sxs-lookup"><span data-stu-id="ceddd-107">ATL 7.1 and earlier versions are not designed with the DEP security feature.</span></span> <span data-ttu-id="ceddd-108">Heureusement, les nouvelles versions des Service Packs Microsoft Windows possèdent de nouvelles API DEP/NX qui vous permettent d’utiliser DEP/NX et de conserver la compatibilité avec les anciennes versions d’ATL.</span><span class="sxs-lookup"><span data-stu-id="ceddd-108">Fortunately, new versions of Microsoft Windows service packs have new DEP/NX APIs that enable you to use DEP/NX and retain compatibility with older ATL versions.</span></span> <span data-ttu-id="ceddd-109">Ces nouvelles API permettent à Internet Explorer de s’abonner à DEP/NX sans entraîner l’échec des modules complémentaires générés à l’aide de versions antérieures d’ATL.</span><span class="sxs-lookup"><span data-stu-id="ceddd-109">These new APIs enable Internet Explorer to opt into DEP/NX without causing add-ons that are built by using older versions of ATL to fail.</span></span>

<span data-ttu-id="ceddd-110">Lorsqu’un module complémentaire n’est pas compatible avec DEP/NX et qu’il n’utilise pas d’ATL obsolète, vous pouvez utiliser une option stratégie de groupe pour refuser DEP/NX pour Internet Explorer jusqu’à ce qu’une version mise à jour du contrôle endommagé soit déployée.</span><span class="sxs-lookup"><span data-stu-id="ceddd-110">When an add-on is not DEP/NX-compatible and it does not use an outdated ATL, you can use a Group Policy option to opt out of DEP/NX for Internet Explorer until an updated version of the broken control is deployed.</span></span> <span data-ttu-id="ceddd-111">Les administrateurs locaux peuvent contrôler DEP/NX en exécutant Internet Explorer en tant qu’administrateur et en désactivant l’option **activer la protection** de la mémoire dans le volet **avancé** des **Options Internet**.</span><span class="sxs-lookup"><span data-stu-id="ceddd-111">Local administrators can control DEP/NX by running Internet Explorer as an administrator and by clearing the **Enable memory protection** option in the **Advanced** pane of **Internet Options**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ceddd-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ceddd-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ceddd-113">Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité</span><span class="sxs-lookup"><span data-stu-id="ceddd-113">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
