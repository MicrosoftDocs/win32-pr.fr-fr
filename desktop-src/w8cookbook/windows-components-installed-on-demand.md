---
title: Composants Windows installés à la demande
description: Composants Windows installés à la demande
ms.assetid: 14865DD7-167C-462C-B85A-BD07C929D7B8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d2c3c3fee1cd12d7b12900e41dc006badcf53f
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104031988"
---
# <a name="windows-components-installed-on-demand"></a><span data-ttu-id="91059-103">Composants Windows installés à la demande</span><span class="sxs-lookup"><span data-stu-id="91059-103">Windows components installed on demand</span></span>

## <a name="platform"></a><span data-ttu-id="91059-104">Plateforme</span><span class="sxs-lookup"><span data-stu-id="91059-104">Platform</span></span>

<span data-ttu-id="91059-105">**Clients-** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="91059-105">**Clients -** Windows 8.1</span></span>  







## <a name="description"></a><span data-ttu-id="91059-106">Description</span><span class="sxs-lookup"><span data-stu-id="91059-106">Description</span></span>

<span data-ttu-id="91059-107">Deux composants Windows seront installés à la demande dans Windows 8.1 : DirectPlay et NTVDM.</span><span class="sxs-lookup"><span data-stu-id="91059-107">Two Windows components will be installed on demand in Windows 8.1: DirectPlay and NTVDM.</span></span> <span data-ttu-id="91059-108">Ces composants sont répertoriés dans les composants facultatifs sous le nœud « composants hérités ».</span><span class="sxs-lookup"><span data-stu-id="91059-108">These components are listed within Optional Components under the “Legacy Components” node.</span></span> <span data-ttu-id="91059-109">Ces composants sont installés localement dans le cadre du système d’exploitation et compressés en tant que composants facultatifs.</span><span class="sxs-lookup"><span data-stu-id="91059-109">These components are installed locally as part of the operating system, and compressed as optional components.</span></span> <span data-ttu-id="91059-110">Quand une application référence ou appelle l’un de ces composants (généralement au premier lancement de l’application), l’installation est déclenchée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="91059-110">When an app references or calls one of these components (usually at first launch of the app), installation is triggered automatically.</span></span> <span data-ttu-id="91059-111">Les utilisateurs sont avertis que le composant sera installé et doivent confirmer l’action pour continuer.</span><span class="sxs-lookup"><span data-stu-id="91059-111">Users will be notified that the component will be installed, and they must confirm the action in order to proceed.</span></span> <span data-ttu-id="91059-112">L’élévation est nécessaire pour que cette opération aboutisse si l’utilisateur n’est pas un administrateur.</span><span class="sxs-lookup"><span data-stu-id="91059-112">Elevation is required for this to succeed if the user is not an administrator.</span></span> <span data-ttu-id="91059-113">Après l’installation initiale, l’utilisateur n’a pas besoin d’effectuer d’autres actions pour réutiliser le composant.</span><span class="sxs-lookup"><span data-stu-id="91059-113">After the initial installation, the user does not need to perform any other actions to use the component again.</span></span>

## <a name="manifestation"></a><span data-ttu-id="91059-114">Manifestation</span><span class="sxs-lookup"><span data-stu-id="91059-114">Manifestation</span></span>

<span data-ttu-id="91059-115">Quand une application référence ou appelle un composant hérité dans des composants facultatifs (au premier lancement), l’application est interrompue et la boîte de dialogue fonctionnalité à la demande s’ouvre et demande l’autorisation de l’utilisateur pour installer le composant.</span><span class="sxs-lookup"><span data-stu-id="91059-115">When an app references or calls a legacy component in optional components (at first launch), the app will be suspended and the Feature on Demand dialog will open, requesting user permission to install the component.</span></span> <span data-ttu-id="91059-116">Si les utilisateurs cliquent sur OK, ils peuvent également voir une invite d’élévation dans laquelle ils doivent entrer leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="91059-116">If users click OK, they may also see an elevation prompt where they must enter their credentials.</span></span> <span data-ttu-id="91059-117">Le composant sera alors installé et l’application reprendra.</span><span class="sxs-lookup"><span data-stu-id="91059-117">The component will then be installed and the app will resume.</span></span>

## <a name="mitigation"></a><span data-ttu-id="91059-118">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="91059-118">Mitigation</span></span>

<span data-ttu-id="91059-119">Pour que l’interface utilisateur des fonctionnalités à la demande ne s’ouvre pas, vous pouvez préinstaller DirectPlay et NTVDM à l’aide de DISM ou de l’interface utilisateur des composants facultatifs.</span><span class="sxs-lookup"><span data-stu-id="91059-119">To keep the Features on Demand UI from opening, you can pre-install DirectPlay and NTVDM using DISM or the Optional Components UI.</span></span>

## <a name="solution"></a><span data-ttu-id="91059-120">Solution</span><span class="sxs-lookup"><span data-stu-id="91059-120">Solution</span></span>

<span data-ttu-id="91059-121">Il est vivement recommandé d’éviter de référencer ou d’appeler des composants qui ont été répertoriés en tant que composants facultatifs hérités dans Windows dans les futures versions de votre application.</span><span class="sxs-lookup"><span data-stu-id="91059-121">You are strongly encouraged to avoid referencing or calling components that have been listed as Legacy Optional Components in Windows in future versions of your app.</span></span> <span data-ttu-id="91059-122">Les composants facultatifs hérités incluent uniquement des composants plus anciens et moins utilisés qui pourraient provoquer des problèmes de performances et de sécurité pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="91059-122">Legacy Optional Components will only include older, lesser-used components that could potentially cause performance and security issues for users.</span></span>

## <a name="tests"></a><span data-ttu-id="91059-123">Tests</span><span class="sxs-lookup"><span data-stu-id="91059-123">Tests</span></span>

<span data-ttu-id="91059-124">Aucun aménagement de test supplémentaire n’est nécessaire pour la compatibilité.</span><span class="sxs-lookup"><span data-stu-id="91059-124">No additional test accommodations are necessary for compatibility.</span></span> <span data-ttu-id="91059-125">Il est important de savoir que cette boîte de dialogue apparaît lorsque le composant facultatif est appelé ou référencé, et que cette installation requiert une élévation.</span><span class="sxs-lookup"><span data-stu-id="91059-125">It is important to be aware that this dialog will appear when the optional component is called or referenced, and this installation requires elevation.</span></span>

 

 




