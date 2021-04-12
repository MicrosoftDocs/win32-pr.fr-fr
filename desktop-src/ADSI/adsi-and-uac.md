---
title: Contrôle de compte d’utilisateur et ADSI
description: Windows et Windows Server possèdent un contrôle de compte d’utilisateur, qui a des ramifications pour les applications qui utilisent des interfaces de service Active Directory (ADSI).
ms.assetid: 0b286252-8c24-4a18-9dc6-063ca158a8ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36fc88169a8710228a3bf70283aaccd4b4ac42e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031852"
---
# <a name="adsi-and-user-account-control"></a><span data-ttu-id="658b0-103">Contrôle de compte d’utilisateur et ADSI</span><span class="sxs-lookup"><span data-stu-id="658b0-103">ADSI and User Account Control</span></span>

<span data-ttu-id="658b0-104">Windows et Windows Server possèdent un [contrôle de compte d’utilisateur](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)), qui a des ramifications pour les applications qui utilisent des interfaces de [service Active Directory](active-directory-service-interfaces-adsi.md) (ADSI).</span><span class="sxs-lookup"><span data-stu-id="658b0-104">Windows and Windows Server have [User Account Control](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)), which has ramifications for applications that use [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI).</span></span> <span data-ttu-id="658b0-105">Plus précisément, ces interfaces ont été conçues pour être exécutées par un compte d’utilisateur disposant de privilèges d’administrateur sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="658b0-105">Specifically, these interfaces were designed to be run by a user account with administrator privileges on the local computer.</span></span>

<span data-ttu-id="658b0-106">**Problème**</span><span class="sxs-lookup"><span data-stu-id="658b0-106">**Problem**</span></span>

<span data-ttu-id="658b0-107">Chaque fois qu’une application se connecte à l’annuaire et tente de créer un objet ADSI, les modifications sont recherchées dans le [schéma de Active Directory](/windows/desktop/ADSchema/active-directory-schema) .</span><span class="sxs-lookup"><span data-stu-id="658b0-107">Every time an application connects to the directory and attempts to create an ADSI object, the [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) is checked for changes.</span></span> <span data-ttu-id="658b0-108">Si elle a changé depuis la dernière connexion, le schéma est téléchargé et stocké dans un cache sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="658b0-108">If it has changed since the last connection, the schema is downloaded and stored in a cache on the local computer.</span></span> <span data-ttu-id="658b0-109">Dans les versions de Windows antérieures à Windows Vista, l’emplacement par défaut de ce cache était</span><span class="sxs-lookup"><span data-stu-id="658b0-109">In versions of Windows prior to Windows Vista, the default location for this cache was</span></span>

`%systemroot%\SchCache\`

<span data-ttu-id="658b0-110">Toutefois, les applications exécutées par les comptes standard (c’est-à-dire non-administrateur) n’ont pas accès à ce répertoire. par conséquent, les applications qui utilisent des interfaces ADSI qui sont exécutées dans ce mode téléchargent le schéma à chaque connexion, ce qui aura un impact sur le débit et les performances.</span><span class="sxs-lookup"><span data-stu-id="658b0-110">However, applications run by standard (that is, non-administrator) accounts will not have access to this directory, and consequently, applications that use ADSI interfaces that are run in this mode will download the schema on every connection, which will impact throughput and performance.</span></span>

<span data-ttu-id="658b0-111">**Solutions**</span><span class="sxs-lookup"><span data-stu-id="658b0-111">**Solutions**</span></span>

<span data-ttu-id="658b0-112">*Utilisateur unique* : pour résoudre ce problème, il existe de nouvelles clés de contrôle de Registre du fournisseur ADSI qui déterminent les emplacements de Registre et les emplacements de fichiers pour les objets de [schéma Active Directory](/windows/desktop/ADSchema/active-directory-schema) mis en cache.</span><span class="sxs-lookup"><span data-stu-id="658b0-112">*Single user* - To resolve this issue, there are new ADSI Provider registry control keys that determine the registry locations and file locations for cached [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) objects.</span></span> <span data-ttu-id="658b0-113">Si la clé de Registre</span><span class="sxs-lookup"><span data-stu-id="658b0-113">If the registry key</span></span>

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

<span data-ttu-id="658b0-114">a la valeur 0 (zéro), chaque utilisateur aura un emplacement de stockage différent pour ADSI ; les clés de Registre seront stockées dans</span><span class="sxs-lookup"><span data-stu-id="658b0-114">is set to 0 (zero), each user will have a different storage location for ADSI; registry keys will be stored in</span></span>

`HKEY_CURRENT_USER\Software\Microsoft\ADs\Providers\LDAP\`

<span data-ttu-id="658b0-115">et les fichiers cache sont stockés dans</span><span class="sxs-lookup"><span data-stu-id="658b0-115">and cache files will be stored in</span></span>

`%LOCALAPPDATA%\Microsoft\Windows\SchCache`

<span data-ttu-id="658b0-116">Ces paramètres sont les paramètres par défaut sur les ordinateurs exécutant Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="658b0-116">These settings are the default settings on computers running Windows Server 2008 or Windows Vista.</span></span>

<span data-ttu-id="658b0-117">*Multi-utilisateur* : Si vous exécutez des applications ADSI sur un ordinateur avec de nombreux comptes d’utilisateur (par exemple, un serveur Web), il est préférable de ne pas avoir de nombreuses copies du cache du [schéma Active Directory](/windows/desktop/ADSchema/active-directory-schema) à l’aide d’une grande quantité d’espace disque.</span><span class="sxs-lookup"><span data-stu-id="658b0-117">*Multi-user* - If you are running ADSI applications on a computer with many user accounts (for example, a web server), then it's preferable not to have many copies of the [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) cache using up large amounts of disk space.</span></span> <span data-ttu-id="658b0-118">Définition de la clé de Registre</span><span class="sxs-lookup"><span data-stu-id="658b0-118">Setting the registry key</span></span>

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

<span data-ttu-id="658b0-119">la valeur 1 (un) restaure le comportement précédent de l’interface ADSI. tous les objets de [schéma Active Directory](/windows/desktop/ADSchema/active-directory-schema) seront stockés dans leurs emplacements précédents. la clé de Registre se trouve dans</span><span class="sxs-lookup"><span data-stu-id="658b0-119">to 1 (one) will revert ADSI to the previous behavior; all [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) objects will be stored in their previous locations; the registry key will be in</span></span>

`HKEY_LOCAL_MACHINE\Software\Microsoft\ADs\Providers\LDAP`

<span data-ttu-id="658b0-120">et le fichier cache se trouve dans</span><span class="sxs-lookup"><span data-stu-id="658b0-120">and the cache file will be in</span></span>

`%systemroot%\SchCache`

<span data-ttu-id="658b0-121">Dans ce cas, les comptes d’administrateur doivent exécuter l’application, ce qui entraîne la mise en cache du fichier de schéma dans l’emplacement global pour une utilisation ultérieure par les utilisateurs moins privilégiés.</span><span class="sxs-lookup"><span data-stu-id="658b0-121">In this case, administrator accounts should run the application, which will cause the schema file to be cached in the global location for future use by the less privileged users.</span></span>

 

 