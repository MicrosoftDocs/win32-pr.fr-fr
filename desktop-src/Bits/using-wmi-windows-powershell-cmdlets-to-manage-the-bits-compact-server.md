---
title: Utilisation des applets de commande WMI Windows PowerShell pour gérer BITS Compact Server
description: Windows PowerShell fournit un mécanisme simple pour se connecter à Windows Management Instrumentation (WMI) sur un ordinateur distant et gérer le serveur compact Service de transfert intelligent en arrière-plan (BITS).
ms.assetid: fe174d2f-4ca0-431e-b1b8-1893ec54147a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c3c942672c147ec5daa0caa2a370e487be80809
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941160"
---
# <a name="using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server"></a><span data-ttu-id="a00ae-103">Utilisation des applets de commande WMI Windows PowerShell pour gérer BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="a00ae-103">Using WMI Windows PowerShell Cmdlets to Manage the BITS Compact Server</span></span>

<span data-ttu-id="a00ae-104">Windows PowerShell fournit un mécanisme simple pour se connecter à Windows Management Instrumentation (WMI) sur un ordinateur distant et gérer le serveur compact Service de transfert intelligent en arrière-plan (BITS).</span><span class="sxs-lookup"><span data-stu-id="a00ae-104">Windows PowerShell provides a simple mechanism to connect to Windows Management Instrumentation (WMI) on a remote computer and manage the Background Intelligent Transfer Service (BITS) Compact Server.</span></span> <span data-ttu-id="a00ae-105">BITS Compact Server est un composant serveur facultatif qui doit être installé séparément.</span><span class="sxs-lookup"><span data-stu-id="a00ae-105">The BITS Compact Server is an optional server component that must be installed separately.</span></span> <span data-ttu-id="a00ae-106">Pour plus d’informations sur l’installation de Compact Server, consultez la documentation de [bits Compact Server](bits-compact-server.md) .</span><span class="sxs-lookup"><span data-stu-id="a00ae-106">For information about installing the Compact Server, see the [BITS Compact Server](bits-compact-server.md) documentation.</span></span>

1.  <span data-ttu-id="a00ae-107">Connectez-vous au fournisseur BITS.</span><span class="sxs-lookup"><span data-stu-id="a00ae-107">Connect to the BITS provider.</span></span>

    ```PowerShell
    $cred = Get-Credential
    $bcs = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" `
    -List -ComputerName Server1 -Credential $cred
    ```

    

    <span data-ttu-id="a00ae-108">L’applet de commande [obtient-Credential](/previous-versions//dd315327(v=technet.10)) demande les informations d’identification de l’utilisateur pour se connecter à l’ordinateur distant et assigne les informations d’identification à l’objet $CRED.</span><span class="sxs-lookup"><span data-stu-id="a00ae-108">The [Get-Credential](/previous-versions//dd315327(v=technet.10)) cmdlet requests the user's credentials to connect to the remote computer and assigns the credentials to the $cred object.</span></span>

    <span data-ttu-id="a00ae-109">Les objets retournés par l’applet de commande [obten-WmiObject](/previous-versions//dd315295(v=technet.10)) sont assignés à la variable $BCS.</span><span class="sxs-lookup"><span data-stu-id="a00ae-109">The objects returned by the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet are assigned to the $bcs variable.</span></span> <span data-ttu-id="a00ae-110">Dans l’exemple précédent, l’applet de commande [obtenir-WmiObject](/previous-versions//dd315295(v=technet.10)) récupère la classe [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) dans l' \\ \\ espace de noms Microsoft bits racine de Server1.</span><span class="sxs-lookup"><span data-stu-id="a00ae-110">In the preceding example, the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet retrieves the [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) class in the root\\Microsoft\\BITS namespace of Server1.</span></span> <span data-ttu-id="a00ae-111">Les méthodes statiques exposées par la classe [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) peuvent être appelées sur l’objet $BCS.</span><span class="sxs-lookup"><span data-stu-id="a00ae-111">Static methods exposed by the [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) class can be called on the $bcs object.</span></span> <span data-ttu-id="a00ae-112">Pour plus d’informations sur la gestion à distance BITS, consultez la rubrique classes du fournisseur [bits](/previous-versions/windows/desktop/bitsprov/bits-provider) et du [fournisseur bits]( /previous-versions//dd904507(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a00ae-112">For more information about BITS remote management, see [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider) and [BITS provider classes]( /previous-versions//dd904507(v=vs.85)).</span></span>

    > [!Note]  
    > <span data-ttu-id="a00ae-113">Le caractère d’accent grave ( \` ) est utilisé pour indiquer un saut de ligne.</span><span class="sxs-lookup"><span data-stu-id="a00ae-113">The grave-accent character (\`) is used to indicate a line break.</span></span>

     

2.  <span data-ttu-id="a00ae-114">Créez un groupe d’URL sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="a00ae-114">Create a URL group on the server.</span></span>

    ```PowerShell
    $URLGroup = "https://Server1:80/testurlgroup" 
    $bcs.CreateUrlGroup($URLGroup)
    ```

    

    <span data-ttu-id="a00ae-115">La https://Server1:80/testurlgroup chaîne de préfixe d’URL "" est assignée à la variable $URLGroup.</span><span class="sxs-lookup"><span data-stu-id="a00ae-115">The "https://Server1:80/testurlgroup" URL prefix string is assigned to the $URLGroup variable.</span></span> <span data-ttu-id="a00ae-116">La variable $URLGroup est transmise à la méthode [CreateUrlGroup](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) , qui crée le groupe d’URL sur Server1.</span><span class="sxs-lookup"><span data-stu-id="a00ae-116">The $URLGroup variable is passed to the [CreateUrlGroup](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) method, which creates the URL group on Server1.</span></span>

    <span data-ttu-id="a00ae-117">Vous pouvez spécifier un autre groupe d’URL.</span><span class="sxs-lookup"><span data-stu-id="a00ae-117">You can specify a different URL group.</span></span> <span data-ttu-id="a00ae-118">Le groupe d’URL doit être conforme à une chaîne de préfixe d’URL valide.</span><span class="sxs-lookup"><span data-stu-id="a00ae-118">The URL group must conform to a valid URL prefix string.</span></span> <span data-ttu-id="a00ae-119">Pour plus d’informations sur les préfixes d’URL, consultez [chaînes URLPrefix](../http/urlprefix-strings.md).</span><span class="sxs-lookup"><span data-stu-id="a00ae-119">For more information about URL prefixes, see [UrlPrefix Strings](../http/urlprefix-strings.md).</span></span>

3.  <span data-ttu-id="a00ae-120">Hébergez un fichier sur le groupe d’URL.</span><span class="sxs-lookup"><span data-stu-id="a00ae-120">Host a file on the URL group.</span></span>

    ```PowerShell
    $bcsObj = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" -filter ("UrlGroup='" + $URLGroup + "'") -ComputerName Server1 -Credential $cred
    $bcsObj.CreateURL("url.txt", "c:\\temp\\1.txt", "") -ComputerName Server1 -Credential $cred
    ```

    

    <span data-ttu-id="a00ae-121">L’instance BITSCompactServerUrlGroup retournée par l’applet de commande [« obtient-WmiObject »](/previous-versions//dd315295(v=technet.10)) est assignée à la variable $bcsObj.</span><span class="sxs-lookup"><span data-stu-id="a00ae-121">The BITSCompactServerUrlGroup instance returned by the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet is assigned to the $bcsObj variable.</span></span> <span data-ttu-id="a00ae-122">La méthode [CreateUrl](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) est appelée pour le $bcsObj avec le suffixe d’URL « url.txt », le \\ \\ \\ \\ chemin d’accès source « c : Temp1.txt » pour le fichier et une chaîne de descripteur de sécurité vide en tant que paramètres.</span><span class="sxs-lookup"><span data-stu-id="a00ae-122">The [CreateUrl](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) method is called for the $bcsObj with the "url.txt" URL suffix, the "c:\\\\temp\\\\1.txt" source path for the file, and an empty security descriptor string as parameters.</span></span> <span data-ttu-id="a00ae-123">Le suffixe « url.txt » est ajouté au préfixe du groupe d’URL.</span><span class="sxs-lookup"><span data-stu-id="a00ae-123">The "url.txt" suffix is added to the URL group prefix.</span></span> <span data-ttu-id="a00ae-124">Les clients peuvent télécharger le fichier à partir de l’adresse suivante : https://Server1:80/testurlgroup/url.txt .</span><span class="sxs-lookup"><span data-stu-id="a00ae-124">Clients can download the file from the following address: https://Server1:80/testurlgroup/url.txt.</span></span>

4.  <span data-ttu-id="a00ae-125">Nettoyez l’URL et le groupe d’URL.</span><span class="sxs-lookup"><span data-stu-id="a00ae-125">Clean up the URL and the URL group.</span></span>

    ```PowerShell
    $bcsObj.Delete()
    ```

    

    <span data-ttu-id="a00ae-126">La méthode de **suppression System. Object** supprime l’objet $bcsObj.</span><span class="sxs-lookup"><span data-stu-id="a00ae-126">The **system.object Delete** method deletes the $bcsObj object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a00ae-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a00ae-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a00ae-128">BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="a00ae-128">BITS Compact Server</span></span>](./bits-compact-server.md)
</dt> <dt>

[<span data-ttu-id="a00ae-129">Fournisseur BITS</span><span class="sxs-lookup"><span data-stu-id="a00ae-129">BITS provider</span></span>](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dt>

<span data-ttu-id="a00ae-130">[Classes du fournisseur BITS]( /previous-versions//dd904507(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a00ae-130">[BITS provider classes]( /previous-versions//dd904507(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="a00ae-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="a00ae-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span></span>
</dt> <dt>

<span data-ttu-id="a00ae-132">[Get-WmiObject](/previous-versions//dd315295(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="a00ae-132">[Get-WmiObject](/previous-versions//dd315295(v=technet.10))</span></span>
</dt> </dl>

 

 