---
description: Tous les paramètres d’authentification sont effectués via le Gestionnaire des services Internet.
ms.assetid: 9b118120-f0cb-4973-b537-dd3d12a7a6d5
ms.tgt_platform: multiple
title: Configuration d’IIS 5,0 et versions ultérieures pour les scripts ASP WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4b5ddde139b3eef32fd7c80f4cca4e10fd816a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527830"
---
# <a name="configuring-iis-50-and-later-for-wmi-asp-scripting"></a><span data-ttu-id="0190e-103">Configuration d’IIS 5,0 et versions ultérieures pour les scripts ASP WMI</span><span class="sxs-lookup"><span data-stu-id="0190e-103">Configuring IIS 5.0 and Later for WMI ASP Scripting</span></span>

<span data-ttu-id="0190e-104">Tous les paramètres d’authentification sont effectués via le Gestionnaire des services Internet.</span><span class="sxs-lookup"><span data-stu-id="0190e-104">All authentication settings are made through the Internet Services Manager.</span></span>

<span data-ttu-id="0190e-105">Lors de la configuration d’Internet Information Server (IIS) 5,0 et de la sécurité IIS 6,0 pour les scripts ASP WMI, tenez compte des points suivants :</span><span class="sxs-lookup"><span data-stu-id="0190e-105">When configuring Internet Information Server (IIS) 5.0 and IIS 6.0 security for WMI ASP scripts, consider the following issues:</span></span>

-   [<span data-ttu-id="0190e-106">Niveau d'authentification</span><span class="sxs-lookup"><span data-stu-id="0190e-106">Authentication level</span></span>](#authentication-level)

    <span data-ttu-id="0190e-107">Vous pouvez configurer au niveau du serveur, du répertoire ou du fichier.</span><span class="sxs-lookup"><span data-stu-id="0190e-107">You can configure at the server, directory, or file level.</span></span>

-   [<span data-ttu-id="0190e-108">Paramètre d’authentification</span><span class="sxs-lookup"><span data-stu-id="0190e-108">Authentication setting</span></span>](#authentication-setting)

    <span data-ttu-id="0190e-109">Vous pouvez définir l’authentification sur anonyme, Windows intégrée ou les deux.</span><span class="sxs-lookup"><span data-stu-id="0190e-109">You can set authentication to Anonymous, Integrated Windows, or both.</span></span>

-   [<span data-ttu-id="0190e-110">Protection</span><span class="sxs-lookup"><span data-stu-id="0190e-110">Protection</span></span>](#protection)

    <span data-ttu-id="0190e-111">Vous pouvez configurer la page ASP pour qu’elle s’exécute in-process (protection faible) ou hors processus à l’aide de Dllhost.exe (protection moyenne ou élevée).</span><span class="sxs-lookup"><span data-stu-id="0190e-111">You can set the ASP to run in-process (low protection), or out-of-process by using Dllhost.exe (medium or high protection).</span></span>

## <a name="authentication-level"></a><span data-ttu-id="0190e-112">Niveau d’authentification</span><span class="sxs-lookup"><span data-stu-id="0190e-112">Authentication Level</span></span>

<span data-ttu-id="0190e-113">Pour renforcer la sécurité, vous pouvez configurer l’authentification au niveau du répertoire ou du fichier.</span><span class="sxs-lookup"><span data-stu-id="0190e-113">For added security, you can configure the authentication at the directory or file level.</span></span>

<span data-ttu-id="0190e-114">Si l’authentification est définie au niveau du serveur, tous les fichiers et répertoires suivants adhèrent à l’authentification du serveur, sauf s’ils sont explicitement modifiés au niveau du répertoire ou du fichier.</span><span class="sxs-lookup"><span data-stu-id="0190e-114">If authentication is set at the server level, all subsequent directories and files adhere to the server authentication unless explicitly altered at the directory or file level.</span></span> <span data-ttu-id="0190e-115">Vous pouvez créer une structure de répertoires contenant tous les scripts WMI ASP où les pages HTML et les ASP spécifiques à WMI peuvent être configurés indépendamment du reste du serveur.</span><span class="sxs-lookup"><span data-stu-id="0190e-115">You can create a directory structure to contain all WMI ASP scripts where HTML pages and ASPs specific to WMI can be configured independently from the rest of the server.</span></span> <span data-ttu-id="0190e-116">Pour modifier le niveau d’authentification d’un serveur, d’un répertoire ou d’un fichier, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="0190e-116">Perform the following procedure to change the authentication level of a server, directory, or file.</span></span>

<span data-ttu-id="0190e-117">**Pour définir l’authentification à n’importe quel niveau**</span><span class="sxs-lookup"><span data-stu-id="0190e-117">**To set the authentication at any level**</span></span>

1.  <span data-ttu-id="0190e-118">Dans le panneau de configuration, double-cliquez sur **Outils d’administration**, puis double-cliquez sur le composant logiciel enfichable IIS.</span><span class="sxs-lookup"><span data-stu-id="0190e-118">In Control Panel, double-click **Administrative Tools**, and then double-click the IIS snap-in.</span></span>

2.  <span data-ttu-id="0190e-119">Recherchez l’icône de page ASP, puis ouvrez les propriétés du niveau à définir, qui peut être serveur, répertoire ou fichier.</span><span class="sxs-lookup"><span data-stu-id="0190e-119">Locate the ASP page icon, and then open the properties for the level to set, which can be server, directory, or file.</span></span>

    > [!Note]  
    > <span data-ttu-id="0190e-120">Les paramètres d’authentification se trouvent sous l’onglet sécurité de **répertoire** ou **sécurité de fichier** de la feuille de **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="0190e-120">Authentication settings are located on either the **Directory Security** or **File Security** tab of the **Properties** sheet.</span></span>

     

## <a name="authentication-setting"></a><span data-ttu-id="0190e-121">Paramètre d’authentification</span><span class="sxs-lookup"><span data-stu-id="0190e-121">Authentication Setting</span></span>

<span data-ttu-id="0190e-122">Pour les scripts ASP WMI, la combinaison de l’authentification anonyme désactivée (non cochée) et l’authentification Windows intégrée activée (activée) offrent une plus grande possibilité de définir la sécurité.</span><span class="sxs-lookup"><span data-stu-id="0190e-122">For WMI ASP scripts, the combination of Anonymous authentication turned off (unchecked), and Integrated Windows authentication turned on (checked) provides greater opportunity to set security.</span></span> <span data-ttu-id="0190e-123">Pour utiliser les paramètres d’authentification IIS NT LAN Manager (NTLM), Passport ou Digest, vous devez activer les privilèges d’activation à distance, car l’utilisateur est traité comme une identité réseau et enregistré à distance.</span><span class="sxs-lookup"><span data-stu-id="0190e-123">To use NT LAN Manager (NTLM), Passport, or Digest IIS authentication settings, you must turn on the remote enable privileges, because the user is treated as a network identity and logged remotely.</span></span> <span data-ttu-id="0190e-124">Le paramètre d’activation à distance n’est pas requis pour l’authentification anonyme et de base.</span><span class="sxs-lookup"><span data-stu-id="0190e-124">The remote enable setting is not required for Anonymous and Basic authentication.</span></span> <span data-ttu-id="0190e-125">Toutefois, le système est bien moins sécurisé lorsque vous utilisez l’authentification anonyme et de base.</span><span class="sxs-lookup"><span data-stu-id="0190e-125">However, the system is much less secure when you are using Anonymous and Basic authentication.</span></span>

<span data-ttu-id="0190e-126">Si l’authentification anonyme est utilisée avec ou sans l’authentification Windows intégrée, l’approche la plus sûre consiste à utiliser une ouverture de session qui requiert un utilisateur pour entrer un nom d’utilisateur et un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="0190e-126">If Anonymous authentication is used with or without Integrated Windows authentication, the most secure approach is to use a logon that requires a user to enter a username and password.</span></span> <span data-ttu-id="0190e-127">L’ouverture de session par défaut est l’identité IIS, mais une ouverture de session peut être créée en utilisant des autorisations spécifiques adaptées aux scripts ASP WMI qui peuvent être utilisés comme compte pour les connexions anonymes ou invitées.</span><span class="sxs-lookup"><span data-stu-id="0190e-127">The default logon is the IIS identity, but a logon can be created by using specific permissions suited for the WMI ASP Scripts that can be used as the account for the anonymous or guest connections.</span></span>

<span data-ttu-id="0190e-128">Si vous choisissez un identificateur de connexion qui n’est pas une identité IIS, désactivez la case à cocher **autoriser les services Internet à contrôler le mot de passe** , puis entrez le mot de passe correct.</span><span class="sxs-lookup"><span data-stu-id="0190e-128">If you choose a logon identifier that is not an IIS identity, then clear the **Allow IIS to control password** check box, and enter the correct password.</span></span> <span data-ttu-id="0190e-129">Cela force toutes les connexions anonymes ou invitées à utiliser l’identificateur de connexion.</span><span class="sxs-lookup"><span data-stu-id="0190e-129">This forces all anonymous or guest connections to use the logon identifier.</span></span> <span data-ttu-id="0190e-130">En créant une connexion distincte de l’identité IIS, les privilèges d’un compte qui accède à WMI peuvent être contrôlés sans affecter les autres répertoires ou fichiers sur le serveur IIS, sauf si l’authentification est définie au niveau du serveur.</span><span class="sxs-lookup"><span data-stu-id="0190e-130">By creating a logon separate from the IIS identity, the privileges of an account accessing WMI can be controlled without affecting the other directories or files on the IIS server—unless the authentication is set at the server level.</span></span>

<span data-ttu-id="0190e-131">Procédez comme suit pour définir les conditions d’authentification pour la page ASP à l’aide du composant logiciel enfichable IIS dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="0190e-131">Perform the following procedure to set the authentication requirements for the ASP page using the IIS snap-in in the Control Panel.</span></span>

<span data-ttu-id="0190e-132">**Pour accéder au paramètre de compte**</span><span class="sxs-lookup"><span data-stu-id="0190e-132">**To get to the account setting**</span></span>

1.  <span data-ttu-id="0190e-133">Dans le panneau de configuration, double-cliquez sur l’icône **Outils d’administration** , ouvrez le composant logiciel enfichable IIS, localisez votre page ASP, puis ouvrez les propriétés du niveau à définir, qui peut être serveur, répertoire ou fichier.</span><span class="sxs-lookup"><span data-stu-id="0190e-133">In Control Panel, double-click the **Administrative Tools** icon, open the IIS snap-in, locate your ASP page, and open the properties of the level to set, which can be server, directory, or file.</span></span>

    <span data-ttu-id="0190e-134">Les paramètres d’authentification se trouvent sous l’onglet sécurité de **répertoire** ou **sécurité de fichier** de la feuille de **Propriétés** .</span><span class="sxs-lookup"><span data-stu-id="0190e-134">Authentication settings can be found on either the **Directory Security** or **File Security** tab of the **Properties** sheet.</span></span>

2.  <span data-ttu-id="0190e-135">Dans la zone authentification anonyme, cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="0190e-135">In the Anonymous authentication area, click **Edit**.</span></span>

3.  <span data-ttu-id="0190e-136">Si un identificateur de connexion autre que l’identité IIS est sélectionné, désactivez la case à cocher **autoriser les services Internet à contrôler le mot de passe**, puis entrez le mot de passe correct.</span><span class="sxs-lookup"><span data-stu-id="0190e-136">If a logon identifier other than the IIS identity is selected, then clear the **Allow IIS to control password** check box, and enter the correct password.</span></span> <span data-ttu-id="0190e-137">Cela force toutes les connexions anonymes ou invitées à utiliser l’identificateur de connexion.</span><span class="sxs-lookup"><span data-stu-id="0190e-137">This forces all anonymous or guest connections to use the logon identifier.</span></span>

<span data-ttu-id="0190e-138">En utilisant une ouverture de session différente de l’identité IIS, les privilèges du compte qui accède à WMI peuvent être contrôlés sans affecter les autres répertoires ou fichiers sur le serveur IIS, sauf si l’authentification est définie au niveau du serveur.</span><span class="sxs-lookup"><span data-stu-id="0190e-138">By using a logon different from the IIS identity, the privileges of the account accessing WMI can be controlled without affecting the other directories or files on the IIS server—unless the authentication is set at the server level.</span></span>

<span data-ttu-id="0190e-139">La configuration précédente permet au serveur IIS d’utiliser l’authentification anonyme dans certains domaines, ainsi que l’authentification Windows ou mixte intégrée dans d’autres.</span><span class="sxs-lookup"><span data-stu-id="0190e-139">The previous configuration allows the IIS server to use Anonymous authentication in some areas, and Integrated Windows or mixed authentication in others.</span></span>

## <a name="protection"></a><span data-ttu-id="0190e-140">Protection</span><span class="sxs-lookup"><span data-stu-id="0190e-140">Protection</span></span>

<span data-ttu-id="0190e-141">La dernière considération à prendre en compte lors de la configuration du serveur IIS est la protection à utiliser lors de l’exécution d’une ASP.</span><span class="sxs-lookup"><span data-stu-id="0190e-141">The last consideration when configuring the IIS server is which protection to use when executing an ASP.</span></span>

<span data-ttu-id="0190e-142">Vous pouvez définir un ASP pour exécuter ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="0190e-142">You can set an ASP to run the following:</span></span>

-   <span data-ttu-id="0190e-143">Dans le processus vers IIS (protection faible).</span><span class="sxs-lookup"><span data-stu-id="0190e-143">In-process to IIS (low protection).</span></span>

-   <span data-ttu-id="0190e-144">Externe à IIS avec Dllhost.exe en tant que pool ou hors processus (protection moyenne regroupée).</span><span class="sxs-lookup"><span data-stu-id="0190e-144">External to IIS with Dllhost.exe as pooled or out-of-process (pooled medium protection).</span></span>

-   <span data-ttu-id="0190e-145">Self-of-process auto-Host (protection élevée).</span><span class="sxs-lookup"><span data-stu-id="0190e-145">Out-of-process self-host (high protection).</span></span>

> [!Note]  
> <span data-ttu-id="0190e-146">Pour un meilleur équilibre entre sécurité et performances, utilisez un hôte mis en pool.</span><span class="sxs-lookup"><span data-stu-id="0190e-146">For the best balance of security and performance, use pooled host.</span></span>

 

 

 



