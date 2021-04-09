---
title: Utilisation de l’extension ADSI pour Services Bureau à distance Configuration utilisateur
description: L’administration des propriétés utilisateur spécifiques à Services Bureau à distance est possible en utilisant les méthodes implémentées par l’extension ADSI (Active Directory Service Interfaces), qui est empaquetée avec la bibliothèque de liens dynamiques Tsuserex.dll.
ms.assetid: f6355730-9686-4446-b118-630562548fc9
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance Services Bureau à distance à l’aide de l’extension ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f115fecf1cce5c518e93206402f76e077109611
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941296"
---
# <a name="using-the-adsi-extension-for-remote-desktop-services-user-configuration"></a><span data-ttu-id="d33a2-104">Utilisation de l’extension ADSI pour Services Bureau à distance Configuration utilisateur</span><span class="sxs-lookup"><span data-stu-id="d33a2-104">Using the ADSI Extension for Remote Desktop Services User Configuration</span></span>

<span data-ttu-id="d33a2-105">L’extension ADSI (Active Directory Service Interfaces) pour Services Bureau à distance Configuration utilisateur est une bibliothèque qui est empaquetée à l’aide de la bibliothèque de liens dynamiques Tsuserex.dll.</span><span class="sxs-lookup"><span data-stu-id="d33a2-105">The Active Directory Service Interfaces (ADSI) extension for Remote Desktop Services user configuration is a library that is packaged with the dynamic-link library Tsuserex.dll.</span></span> <span data-ttu-id="d33a2-106">L’administration des propriétés utilisateur spécifiques à Services Bureau à distance est possible à l’aide des méthodes implémentées par l’extension.</span><span class="sxs-lookup"><span data-stu-id="d33a2-106">Administration of Remote Desktop Services-specific user properties is possible using the methods implemented by the extension.</span></span> <span data-ttu-id="d33a2-107">Les méthodes permettent de configurer les propriétés qui sont disponibles dans l’interface d’extension pour les utilisateurs Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="d33a2-107">The methods allow configuration of the properties that are available in the extension interface for Remote Desktop Services users.</span></span>

<span data-ttu-id="d33a2-108">L’extension ADSI pour Services Bureau à distance Configuration utilisateur prend en charge l’examen et la manipulation de Services Bureau à distance propriétés utilisateur stockées dans la base de données du service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="d33a2-108">The ADSI extension for Remote Desktop Services user configuration supports the examination and manipulation of Remote Desktop Services user properties stored in the Directory Service database.</span></span> <span data-ttu-id="d33a2-109">L’extension prend également en charge la configuration des propriétés utilisateur stockées dans le Active Directory, par le biais de l’API LDAP (Lightweight Directory Access Protocol).</span><span class="sxs-lookup"><span data-stu-id="d33a2-109">The extension also supports configuration of user properties that are stored in the Active Directory, through the Lightweight Directory Access Protocol (LDAP) API.</span></span>

<span data-ttu-id="d33a2-110">Le fournisseur implémente les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d33a2-110">The provider implements the following methods:</span></span>

-   <span data-ttu-id="d33a2-111">[**IADs :: obten**](/windows/desktop/api/iads/nf-iads-iads-get).</span><span class="sxs-lookup"><span data-stu-id="d33a2-111">[**IADs::Get**](/windows/desktop/api/iads/nf-iads-iads-get).</span></span> <span data-ttu-id="d33a2-112">Cette méthode recherche une propriété ou un ensemble de propriétés spécifiques sur une instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="d33a2-112">This method searches for a specific property or set of properties on an instance of the class.</span></span>
-   <span data-ttu-id="d33a2-113">[**IADs ::P ut**](/windows/desktop/api/iads/nf-iads-iads-put).</span><span class="sxs-lookup"><span data-stu-id="d33a2-113">[**IADs::Put**](/windows/desktop/api/iads/nf-iads-iads-put).</span></span> <span data-ttu-id="d33a2-114">Cette méthode Configure une propriété spécifique ou un ensemble de propriétés sur une instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="d33a2-114">This method configures a specific property or set of properties on an instance of the class.</span></span>

<span data-ttu-id="d33a2-115">Pour obtenir la liste des propriétés Services Bureau à distance utilisateur spécifiques que vous pouvez configurer, consultez la [référence de l’extension ADSI pour services Bureau à distance Configuration utilisateur](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) .</span><span class="sxs-lookup"><span data-stu-id="d33a2-115">See the [Reference for the ADSI Extension for Remote Desktop Services User Configuration](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) for a list of the specific Remote Desktop Services user properties you can configure.</span></span>

<span data-ttu-id="d33a2-116">Pour plus d’informations sur l’accès et la modification des attributs avec ADSI, consultez [accès et manipulation des données avec ADSI](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi).</span><span class="sxs-lookup"><span data-stu-id="d33a2-116">For more information about accessing and modifying attributes with ADSI, see [Accessing and Manipulating Data with ADSI](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi).</span></span>

<span data-ttu-id="d33a2-117">Pour plus d’informations sur l’utilisation des conventions d’affectation de noms ADSI et des chaînes AdsPath, consultez les informations sur les [fournisseurs de services ADSI](/windows/desktop/ADSI/adsi-system-providers) individuels dans la documentation du kit de développement logiciel (SDK) de la plate-forme [Interfaces de service Active Directory](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) .</span><span class="sxs-lookup"><span data-stu-id="d33a2-117">For more information about using ADSI naming conventions and AdsPath strings, see the information about individual [ADSI Service Providers](/windows/desktop/ADSI/adsi-system-providers) in the [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) Platform Software Development Kit (SDK) documentation.</span></span>

 

 