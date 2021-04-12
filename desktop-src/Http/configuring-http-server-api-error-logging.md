---
title: Configuration de la journalisation des erreurs de l’API du serveur HTTP
description: La journalisation des erreurs de l’API du serveur HTTP est contrôlée par trois valeurs de Registre sous une \\ clé de paramètres http.
ms.assetid: a7712159-939e-42e3-a8d8-73148c2f4f6e
keywords:
- API serveur HTTP, configuration des journaux d’erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f6b5ae81b1933ea745789e0fae33dfc7ebce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379916"
---
# <a name="configuring-http-server-api-error-logging"></a><span data-ttu-id="24269-104">Configuration de la journalisation des erreurs de l’API du serveur HTTP</span><span class="sxs-lookup"><span data-stu-id="24269-104">Configuring HTTP Server API Error Logging</span></span>

<span data-ttu-id="24269-105">La journalisation des erreurs de l’API du serveur http est contrôlée par trois valeurs de Registre sous une \\ clé de **paramètres** http située à l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="24269-105">The HTTP Server API error logging is controlled by three registry values under an **HTTP**\\**Parameters** key located at:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

> [!Note]  
> <span data-ttu-id="24269-106">L’emplacement et la forme des valeurs de configuration peuvent changer dans les versions ultérieures du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="24269-106">The location and form of the configuration values may change in future versions of the Windows operating system.</span></span>

 

<span data-ttu-id="24269-107">Un utilisateur doit disposer des privilèges administrateur/système local pour modifier les valeurs de Registre et afficher ou modifier les fichiers journaux et le dossier qui les contient.</span><span class="sxs-lookup"><span data-stu-id="24269-107">A user must have Administrator/Local System privileges to modify the registry values, and view or modify the log files and the folder that contains them.</span></span>

<span data-ttu-id="24269-108">Les informations de configuration dans les valeurs de Registre sont lues lorsque le pilote de l’API du serveur HTTP est démarré.</span><span class="sxs-lookup"><span data-stu-id="24269-108">Configuration information in the registry values is read when the HTTP Server API driver is started.</span></span> <span data-ttu-id="24269-109">Par conséquent, si les paramètres sont modifiés, le pilote doit être arrêté et redémarré pour lire les nouvelles valeurs.</span><span class="sxs-lookup"><span data-stu-id="24269-109">As a result, if the settings are changed the driver must be stopped and restarted to read the new values.</span></span> <span data-ttu-id="24269-110">Pour ce faire, vous pouvez utiliser les commandes de console suivantes :</span><span class="sxs-lookup"><span data-stu-id="24269-110">This can be accomplished by using the following console commands:</span></span>

<span data-ttu-id="24269-111">**net stop http**</span><span class="sxs-lookup"><span data-stu-id="24269-111">**net stop http**</span></span>

<span data-ttu-id="24269-112">**NET START http**</span><span class="sxs-lookup"><span data-stu-id="24269-112">**net start http**</span></span>

<span data-ttu-id="24269-113">Les fichiers journaux sont nommés à l’aide de la Convention suivante :</span><span class="sxs-lookup"><span data-stu-id="24269-113">The log files are named by using the following convention:</span></span>

<span data-ttu-id="24269-114">**HTTPERR +**  pas **+. log**</span><span class="sxs-lookup"><span data-stu-id="24269-114">**httperr +** *SequenceNumber* **+ .log**</span></span>

<span data-ttu-id="24269-115">Par exemple : « httperr4. log ».</span><span class="sxs-lookup"><span data-stu-id="24269-115">For example: "httperr4.log".</span></span>

<span data-ttu-id="24269-116">Les fichiers journaux sont recyclés lorsqu’ils atteignent la taille maximale spécifiée par la valeur de Registre **ErrorLogFileTruncateSize** , et la valeur ne peut pas être inférieure à un mégaoctet (Mo).</span><span class="sxs-lookup"><span data-stu-id="24269-116">Log files are cycled when they reach the maximum size specified by the **ErrorLogFileTruncateSize** registry value, and the value cannot be less than one megabyte (MB).</span></span>

<span data-ttu-id="24269-117">Si la configuration de la journalisation des erreurs n’est pas valide ou si une erreur se produit lors de l’écriture dans les fichiers journaux, l’API du serveur HTTP utilise l’enregistrement des événements pour informer les administrateurs que la journalisation des erreurs n’a pas eu lieu.</span><span class="sxs-lookup"><span data-stu-id="24269-117">If the configuration of error logging is invalid or any kind of failure occurs while writing to the log files, the HTTP Server API uses event logging to notify administrators that error logging did not take place.</span></span>

<span data-ttu-id="24269-118">Les valeurs de configuration du Registre sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="24269-118">Registry configuration values are described in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24269-119">Valeur de Registre</span><span class="sxs-lookup"><span data-stu-id="24269-119">Registry Value</span></span></th>
<th><span data-ttu-id="24269-120">Description</span><span class="sxs-lookup"><span data-stu-id="24269-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="24269-121"><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging</span><span class="sxs-lookup"><span data-stu-id="24269-121"><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging</span></span><br/></td>
<td><span data-ttu-id="24269-122">Valeur <strong>DWORD</strong> qui peut être définie sur <strong>true</strong> pour activer la journalisation des erreurs, ou <strong>false</strong> pour la désactiver.</span><span class="sxs-lookup"><span data-stu-id="24269-122">A <strong>DWORD</strong> that can be set to <strong>TRUE</strong> to enable error logging, or <strong>FALSE</strong> to disable it.</span></span> <span data-ttu-id="24269-123">La valeur par défaut est <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="24269-123">The default value is <strong>TRUE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24269-124"><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize</span><span class="sxs-lookup"><span data-stu-id="24269-124"><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize</span></span><br/></td>
<td><span data-ttu-id="24269-125"><strong>Valeur DWORD</strong> qui spécifie la taille maximale, en octets, d’un fichier journal des erreurs.</span><span class="sxs-lookup"><span data-stu-id="24269-125">A <strong>DWORD</strong> that specifies the maximum size of an error log file, in bytes.</span></span> <span data-ttu-id="24269-126">La valeur par défaut est un mégaoctet (de 1 à 1).</span><span class="sxs-lookup"><span data-stu-id="24269-126">The default value is one MB (0x100000).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="24269-127">La valeur spécifiée ne peut pas être inférieure à la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="24269-127">The specified value cannot be smaller than the default value.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24269-128"><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir</span><span class="sxs-lookup"><span data-stu-id="24269-128"><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir</span></span><br/></td>
<td><span data-ttu-id="24269-129"><strong>Chaîne</strong> qui spécifie le dossier sous lequel l’API du serveur http place ses fichiers de journalisation.</span><span class="sxs-lookup"><span data-stu-id="24269-129">A <strong>String</strong> that specifies the folder under which the HTTP Server API places its logging files.</span></span> <br/> <span data-ttu-id="24269-130">L’API du serveur HTTP crée un sous-dossier nommé &quot; HTTPERR &quot; sous le dossier spécifié dans lequel les fichiers journaux sont placés.</span><span class="sxs-lookup"><span data-stu-id="24269-130">The HTTP Server API creates a subfolder named &quot;HTTPERR&quot; under the specified folder into which the log files are placed.</span></span> <span data-ttu-id="24269-131">Ce sous-dossier et les fichiers journaux reçoivent les mêmes paramètres d’autorisation, ce qui signifie que les comptes administrateur et système local ont un accès complet, alors que les autres utilisateurs n’ont pas accès.</span><span class="sxs-lookup"><span data-stu-id="24269-131">This subfolder and the log files receive the same permission settings, which means that Administrator and Local System Accounts have full access, while other users do not have access.</span></span><br/> <span data-ttu-id="24269-132">Si aucun dossier n’est spécifié dans le registre, le dossier par défaut est le suivant :</span><span class="sxs-lookup"><span data-stu-id="24269-132">If a folder is not specified in the registry, the default folder is the following:</span></span><br/> <span data-ttu-id="24269-133">&quot;%SystemRoot%\System32\LogFiles&quot;</span><span class="sxs-lookup"><span data-stu-id="24269-133">&quot;%SystemRoot%\System32\LogFiles&quot;</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="24269-134">La valeur de chaîne ErrorLoggingDir doit être un chemin d’accès complet, mais elle peut contenir &quot; % systemroot% &quot; .</span><span class="sxs-lookup"><span data-stu-id="24269-134">The ErrorLoggingDir string value must be a fully qualified path, but it can contain &quot;%SystemRoot%&quot;.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

 

 





