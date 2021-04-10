---
title: Numéroteurs personnalisés
description: Windows 2000 et les systèmes d’exploitation ultérieurs permettent aux développeurs de fournir leurs propres numéroteurs personnalisés qui fonctionnent avec le service d’accès à distance (RAS).
ms.assetid: ad94f38d-812f-4329-8055-6274a21a3242
keywords:
- Numéroteurs personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35293de408a2a0faa146b93f9b5d5ebccf447acc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199317"
---
# <a name="custom-dialers"></a><span data-ttu-id="c169e-104">Numéroteurs personnalisés</span><span class="sxs-lookup"><span data-stu-id="c169e-104">Custom Dialers</span></span>

<span data-ttu-id="c169e-105">Windows 2000 et les systèmes d’exploitation ultérieurs permettent aux développeurs de fournir leurs propres numéroteurs personnalisés qui fonctionnent avec le service d’accès à distance (RAS).</span><span class="sxs-lookup"><span data-stu-id="c169e-105">Windows 2000 and later operating systems enable developers to provide their own custom dialers that work with the Remote Access Service (RAS).</span></span> <span data-ttu-id="c169e-106">Le numéroteur personnalisé est implémenté en tant que bibliothèque de liens dynamiques (DLL) unique qui exporte les points d’entrée suivants :</span><span class="sxs-lookup"><span data-stu-id="c169e-106">The custom dialer is implemented as a single dynamic-link library (DLL) that exports the following entry points:</span></span>

-   [<span data-ttu-id="c169e-107">**RasCustomDial**</span><span class="sxs-lookup"><span data-stu-id="c169e-107">**RasCustomDial**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomdialfn)
-   [<span data-ttu-id="c169e-108">**RasCustomDialDlg**</span><span class="sxs-lookup"><span data-stu-id="c169e-108">**RasCustomDialDlg**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomdialdlgfn)
-   [<span data-ttu-id="c169e-109">**RasCustomHangup**</span><span class="sxs-lookup"><span data-stu-id="c169e-109">**RasCustomHangup**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomhangupfn)
-   [<span data-ttu-id="c169e-110">**RasCustomEntryDlg**</span><span class="sxs-lookup"><span data-stu-id="c169e-110">**RasCustomEntryDlg**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomentrydlgfn)
-   [<span data-ttu-id="c169e-111">**RasCustomDeleteEntryNotify**</span><span class="sxs-lookup"><span data-stu-id="c169e-111">**RasCustomDeleteEntryNotify**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomdeleteentrynotifyfn)

<span data-ttu-id="c169e-112">La DLL de numérotation personnalisée doit exporter tous ces points d’entrée et elle doit implémenter les points d’entrée en tant que fonctions Unicode.</span><span class="sxs-lookup"><span data-stu-id="c169e-112">The custom-dial DLL must export all of these entry points, and it must implement the entry points as Unicode functions.</span></span> <span data-ttu-id="c169e-113">Pour plus d’informations sur ces fonctions, consultez la page de référence de chaque fonction dans le SDK Windows référence du service d’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="c169e-113">For more information about these functions, see the reference page for each function in the Windows SDK Remote Access Service Reference.</span></span>

<span data-ttu-id="c169e-114">Pour qu’une connexion RAS utilise le numéroteur personnalisé, l’entrée de l’annuaire téléphonique pour la connexion doit contenir le chemin d’accès à la DLL de numérotation personnalisée.</span><span class="sxs-lookup"><span data-stu-id="c169e-114">In order for a RAS connection to use the custom dialer, the phone-book entry for the connection must contain the path to the custom-dial DLL.</span></span> <span data-ttu-id="c169e-115">Utilisez les fonctions d’API RAS [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) et [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) pour définir ce chemin d’accès dans le membre **szCustomDialDll** de la structure [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) pour l’entrée de l’annuaire téléphonique.</span><span class="sxs-lookup"><span data-stu-id="c169e-115">Use the RAS API functions [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) and [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) to set this path in the **szCustomDialDll** member of the [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) structure for the phone-book entry.</span></span>

## <a name="updating-the-registry-for-custom-dialers"></a><span data-ttu-id="c169e-116">Mise à jour du Registre pour les numéroteurs personnalisés</span><span class="sxs-lookup"><span data-stu-id="c169e-116">Updating the Registry for Custom Dialers</span></span>

<span data-ttu-id="c169e-117">Pour que le système puisse établir une connexion qui utilise un numéroteur personnalisé, le chemin d’accès à la DLL de numérotation personnalisée doit exister dans la valeur de Registre suivante.</span><span class="sxs-lookup"><span data-stu-id="c169e-117">In order for the system to dial a connection that uses a custom dialer, the path to the custom-dial DLL must exist in the following registry value.</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
                  CustomDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_MULTI_SZ</dd>
</dl>
```

<span data-ttu-id="c169e-118">Étant donné que **CustomDLL** est de type **reg \_ \_ multisz**, il peut contenir les chemins d’accès à plusieurs dll de numérotation personnalisée.</span><span class="sxs-lookup"><span data-stu-id="c169e-118">Because **CustomDLL** is of type **REG\_MULTI\_SZ**, it can hold paths to multiple custom-dial DLLs.</span></span> <span data-ttu-id="c169e-119">Vous devez définir le chemin d’accès à la DLL de numérotation personnalisée dans cette valeur de Registre, en plus de l’entrée de l’annuaire téléphonique pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="c169e-119">You need to set the path to the custom-dial DLL in this registry value, in addition to the phone-book entry for the connection.</span></span>

<span data-ttu-id="c169e-120">Par défaut, cette valeur de Registre est accessible en écriture uniquement par un utilisateur disposant de privilèges d’administrateur ou de système.</span><span class="sxs-lookup"><span data-stu-id="c169e-120">By default, this registry value is writeable only by a user with Administrator or System privileges.</span></span> <span data-ttu-id="c169e-121">Pour des raisons de sécurité, ne modifiez pas les autorisations sur cette clé de registre.</span><span class="sxs-lookup"><span data-stu-id="c169e-121">For security reasons, do not change the permissions on this registry key.</span></span>

## <a name="using-custom-dialers-at-system-logon"></a><span data-ttu-id="c169e-122">Utilisation de numéroteurs personnalisés lors de l’ouverture de session système</span><span class="sxs-lookup"><span data-stu-id="c169e-122">Using Custom Dialers at System Logon</span></span>

<span data-ttu-id="c169e-123">Windows 2000 et les systèmes d’exploitation ultérieurs permettent à un utilisateur d’établir une connexion RAS au moment de l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="c169e-123">Windows 2000 and later operating systems allow a user to establish a RAS connection at the time of logon.</span></span> <span data-ttu-id="c169e-124">Pour ce faire, l’utilisateur vérifie la **connexion à l’aide de l’accès réseau à distance** dans la boîte de dialogue informations de **connexion** .</span><span class="sxs-lookup"><span data-stu-id="c169e-124">To do so, the user checks **Logon using Dial-up Networking** in the **Logon Information** dialog box.</span></span> <span data-ttu-id="c169e-125">Une fois que l’utilisateur a cliqué sur le bouton OK, le système affiche les connexions disponibles.</span><span class="sxs-lookup"><span data-stu-id="c169e-125">After the user clicks the Okay button, the system displays the available connections.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="c169e-126">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="c169e-126">Security Considerations</span></span>

<span data-ttu-id="c169e-127">Dans la plupart des cas, un numéroteur personnalisé fonctionne avec les privilèges de sécurité de l’utilisateur qui l’appelle.</span><span class="sxs-lookup"><span data-stu-id="c169e-127">In most cases, a custom dialer operates with the security privileges of the user that invokes it.</span></span> <span data-ttu-id="c169e-128">Toutefois, si le numéroteur personnalisé est appelé lors de l’ouverture de session, il fonctionne avec des privilèges système.</span><span class="sxs-lookup"><span data-stu-id="c169e-128">However, if the custom dialer is invoked at logon, it operates with system privileges.</span></span> <span data-ttu-id="c169e-129">Par conséquent, concevez le numéroteur personnalisé afin qu’il ne puisse pas être utilisé pour enfreindre la sécurité du système.</span><span class="sxs-lookup"><span data-stu-id="c169e-129">Therefore, design the custom dialer so that it cannot be used to violate system security.</span></span> <span data-ttu-id="c169e-130">Par exemple, le numéroteur ne doit pas présenter une interface utilisateur qui permet à l’utilisateur d’écrire un accès au système de fichiers de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c169e-130">For example, the dialer should not present a user interface that allows the user write access to the computer's file system.</span></span> <span data-ttu-id="c169e-131">Les interfaces utilisateur qui fournissent un tel accès incluent la boîte de dialogue **Rechercher un fichier** , la boîte de dialogue commune **ouvrir un fichier** et l' **aide** de Windows.</span><span class="sxs-lookup"><span data-stu-id="c169e-131">User interfaces that provide such access include the **Find-File** dialog, the **File-Open** common dialog, and Windows **Help**.</span></span>

## <a name="custom-dialer-user-interface-must-support-idcancel"></a><span data-ttu-id="c169e-132">L’interface utilisateur du numéroteur personnalisé doit prendre en charge IDCANCEL</span><span class="sxs-lookup"><span data-stu-id="c169e-132">Custom Dialer User Interface Must Support IDCANCEL</span></span>

<span data-ttu-id="c169e-133">Si le numéroteur personnalisé affiche une interface utilisateur, l’interface utilisateur doit prendre en charge les \_ messages de commande WM où LOWORD (*wParam*) est égal à IDCANCEL.</span><span class="sxs-lookup"><span data-stu-id="c169e-133">If the custom dialer displays a user interface, the user interface must support WM\_COMMAND messages where LOWORD(*wParam*) equals IDCANCEL.</span></span>

 

 