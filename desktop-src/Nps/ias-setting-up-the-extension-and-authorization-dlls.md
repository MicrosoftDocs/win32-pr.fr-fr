---
title: Configuration des dll d’extension
description: Au démarrage, NPS vérifie dans le registre la liste des dll tierces à appeler.
ms.assetid: fbbd9031-3ebe-47b8-8d8b-e359fa7d4b67
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e8589f31144f12b120f9a77f281dd57a9f30ce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031559"
---
# <a name="setting-up-the-extension-dlls"></a><span data-ttu-id="82956-103">Configuration des dll d’extension</span><span class="sxs-lookup"><span data-stu-id="82956-103">Setting Up the Extension DLLs</span></span>

> [!Note]  
> <span data-ttu-id="82956-104">Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="82956-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="82956-105">Le contenu de cette rubrique s’applique à IAS et à NPS.</span><span class="sxs-lookup"><span data-stu-id="82956-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="82956-106">Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.</span><span class="sxs-lookup"><span data-stu-id="82956-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="82956-107">Au démarrage, NPS vérifie dans le registre la liste des dll tierces à appeler.</span><span class="sxs-lookup"><span data-stu-id="82956-107">At startup, NPS checks the registry for a list of third-party DLLs to call.</span></span>

<span data-ttu-id="82956-108">Pour configurer une DLL d’authentification ou d’autorisation sur un serveur NPS, répertoriez les chemins d’accès aux dll dans les valeurs sous la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="82956-108">To set up an Authentication or Authorization DLL on an NPS server, list the paths to the DLLs in values below the following registry key:</span></span>

<span data-ttu-id="82956-109">**\\Paramètres de \\ AuthSrv des services de CurrentControlSet du système HKLM \\ \\ \\\\**</span><span class="sxs-lookup"><span data-stu-id="82956-109">**HKLM\\System\\CurrentControlSet\\Services\\AuthSrv\\Parameters\\**</span></span>

<span data-ttu-id="82956-110">Si les clés **AuthSrv** et **Parameters** n’existent pas, créez-les.</span><span class="sxs-lookup"><span data-stu-id="82956-110">If the **AuthSrv** and **Parameters** keys do not exist, create them.</span></span>

<span data-ttu-id="82956-111">La valeur d’énumération des dll d’extension d’authentification est la suivante :</span><span class="sxs-lookup"><span data-stu-id="82956-111">The value in which to list the Authentication Extension DLLs is:</span></span>

<span data-ttu-id="82956-112">**ExtensionDLLs**</span><span class="sxs-lookup"><span data-stu-id="82956-112">**ExtensionDLLs**</span></span>

<span data-ttu-id="82956-113">La valeur dans laquelle répertorier les dll d’extension d’autorisation est :</span><span class="sxs-lookup"><span data-stu-id="82956-113">The value in which to list the Authorization Extension DLLs is:</span></span>

<span data-ttu-id="82956-114">**AuthorizationDLLs**</span><span class="sxs-lookup"><span data-stu-id="82956-114">**AuthorizationDLLs**</span></span>

<span data-ttu-id="82956-115">Les valeurs **ExtensionDLLs** et **AuthorizationDLLs** doivent être de type **reg \_ multi \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="82956-115">Both the **ExtensionDLLs** and **AuthorizationDLLs** values must be of type **REG\_MULTI\_SZ**.</span></span> <span data-ttu-id="82956-116">Ce type vous permet de répertorier plusieurs dll.</span><span class="sxs-lookup"><span data-stu-id="82956-116">This type allows you to list multiple DLLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82956-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="82956-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82956-118">Appel des dll d’extension</span><span class="sxs-lookup"><span data-stu-id="82956-118">Invoking the Extension DLLs</span></span>](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> <dt>

[<span data-ttu-id="82956-119">Attributs d’identification utilisateur</span><span class="sxs-lookup"><span data-stu-id="82956-119">User Identification Attributes</span></span>](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 