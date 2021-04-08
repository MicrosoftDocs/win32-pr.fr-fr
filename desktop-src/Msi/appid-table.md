---
description: La table AppId ou la table Registry spécifie que le programme d’installation doit configurer et inscrire les serveurs DCOM pour effectuer l’une des opérations suivantes au cours d’une installation.
ms.assetid: d76ed6df-944b-4996-bf07-e42ceb7a1b69
title: Table AppId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07fa202907c094d8c12f73d838f5ad1d6b942125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864490"
---
# <a name="appid-table"></a><span data-ttu-id="608fe-103">Table AppId</span><span class="sxs-lookup"><span data-stu-id="608fe-103">AppId Table</span></span>

<span data-ttu-id="608fe-104">La table AppId ou la [table Registry](registry-table.md) spécifie que le programme d’installation doit configurer et inscrire les serveurs DCOM pour effectuer l’une des opérations suivantes au cours d’une installation.</span><span class="sxs-lookup"><span data-stu-id="608fe-104">The AppId table or the [Registry table](registry-table.md) specifies that the installer configure and register DCOM servers to do one of the following during an installation.</span></span>

-   <span data-ttu-id="608fe-105">Exécutez le serveur DCOM sous une identité différente de celle de l’utilisateur qui a activé le serveur.</span><span class="sxs-lookup"><span data-stu-id="608fe-105">Run the DCOM server under a different identity than the user activating the server.</span></span> <span data-ttu-id="608fe-106">Par exemple, pour configurer un serveur DCOM pour qu’il s’exécute toujours en tant qu’utilisateur interactif ou en tant qu’utilisateur prédéfini.</span><span class="sxs-lookup"><span data-stu-id="608fe-106">For example, to configure a DCOM server to always run as an interactive user or as a predefined user.</span></span>
-   <span data-ttu-id="608fe-107">Exécutez le serveur DCOM en tant que service.</span><span class="sxs-lookup"><span data-stu-id="608fe-107">Run the DCOM server as a service.</span></span>
-   <span data-ttu-id="608fe-108">Configurez l’accès de sécurité par défaut pour le serveur DCOM.</span><span class="sxs-lookup"><span data-stu-id="608fe-108">Configure the default security access for the DCOM server.</span></span>
-   <span data-ttu-id="608fe-109">Inscrire le serveur DCOM de manière à ce qu’il soit activé sur un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="608fe-109">Register the DCOM server such that it is activated on a different computer.</span></span>

<span data-ttu-id="608fe-110">Cette table est traitée lors de l’installation du composant associé au serveur DCOM dans la \_ colonne composant de la [table de classe](class-table.md).</span><span class="sxs-lookup"><span data-stu-id="608fe-110">This table is processed at the installation of the component associated with the DCOM server in the \_Component column of the [Class table](class-table.md).</span></span> <span data-ttu-id="608fe-111">Un AppId n’est pas publié.</span><span class="sxs-lookup"><span data-stu-id="608fe-111">An AppId is not advertised.</span></span>

<span data-ttu-id="608fe-112">La table AppId contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="608fe-112">The AppId table has the following columns.</span></span>



| <span data-ttu-id="608fe-113">Colonne</span><span class="sxs-lookup"><span data-stu-id="608fe-113">Column</span></span>               | <span data-ttu-id="608fe-114">Type</span><span class="sxs-lookup"><span data-stu-id="608fe-114">Type</span></span>                       | <span data-ttu-id="608fe-115">Clé</span><span class="sxs-lookup"><span data-stu-id="608fe-115">Key</span></span> | <span data-ttu-id="608fe-116">Nullable</span><span class="sxs-lookup"><span data-stu-id="608fe-116">Nullable</span></span> |
|----------------------|----------------------------|-----|----------|
| <span data-ttu-id="608fe-117">AppId</span><span class="sxs-lookup"><span data-stu-id="608fe-117">AppId</span></span>                | [<span data-ttu-id="608fe-118">GUID</span><span class="sxs-lookup"><span data-stu-id="608fe-118">GUID</span></span>](guid.md)           | <span data-ttu-id="608fe-119">O</span><span class="sxs-lookup"><span data-stu-id="608fe-119">Y</span></span>   | <span data-ttu-id="608fe-120">N</span><span class="sxs-lookup"><span data-stu-id="608fe-120">N</span></span>        |
| <span data-ttu-id="608fe-121">RemoteServerName</span><span class="sxs-lookup"><span data-stu-id="608fe-121">RemoteServerName</span></span>     | [<span data-ttu-id="608fe-122">Correct</span><span class="sxs-lookup"><span data-stu-id="608fe-122">Formatted</span></span>](formatted.md) | <span data-ttu-id="608fe-123">N</span><span class="sxs-lookup"><span data-stu-id="608fe-123">N</span></span>   | <span data-ttu-id="608fe-124">O</span><span class="sxs-lookup"><span data-stu-id="608fe-124">Y</span></span>        |
| <span data-ttu-id="608fe-125">LocalService</span><span class="sxs-lookup"><span data-stu-id="608fe-125">LocalService</span></span>         | [<span data-ttu-id="608fe-126">Text</span><span class="sxs-lookup"><span data-stu-id="608fe-126">Text</span></span>](text.md)           | <span data-ttu-id="608fe-127">N</span><span class="sxs-lookup"><span data-stu-id="608fe-127">N</span></span>   | <span data-ttu-id="608fe-128">O</span><span class="sxs-lookup"><span data-stu-id="608fe-128">Y</span></span>        |
| <span data-ttu-id="608fe-129">ServiceParameters</span><span class="sxs-lookup"><span data-stu-id="608fe-129">ServiceParameters</span></span>    | [<span data-ttu-id="608fe-130">Text</span><span class="sxs-lookup"><span data-stu-id="608fe-130">Text</span></span>](text.md)           | <span data-ttu-id="608fe-131">N</span><span class="sxs-lookup"><span data-stu-id="608fe-131">N</span></span>   | <span data-ttu-id="608fe-132">O</span><span class="sxs-lookup"><span data-stu-id="608fe-132">Y</span></span>        |
| <span data-ttu-id="608fe-133">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="608fe-133">DllSurrogate</span></span>         | [<span data-ttu-id="608fe-134">Text</span><span class="sxs-lookup"><span data-stu-id="608fe-134">Text</span></span>](text.md)           | <span data-ttu-id="608fe-135">N</span><span class="sxs-lookup"><span data-stu-id="608fe-135">N</span></span>   | <span data-ttu-id="608fe-136">O</span><span class="sxs-lookup"><span data-stu-id="608fe-136">Y</span></span>        |
| <span data-ttu-id="608fe-137">ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="608fe-137">ActivateAtStorage</span></span>    | [<span data-ttu-id="608fe-138">Integer</span><span class="sxs-lookup"><span data-stu-id="608fe-138">Integer</span></span>](integer.md)     | <span data-ttu-id="608fe-139">N</span><span class="sxs-lookup"><span data-stu-id="608fe-139">N</span></span>   | <span data-ttu-id="608fe-140">O</span><span class="sxs-lookup"><span data-stu-id="608fe-140">Y</span></span>        |
| <span data-ttu-id="608fe-141">RunAsInteractiveUser</span><span class="sxs-lookup"><span data-stu-id="608fe-141">RunAsInteractiveUser</span></span> | [<span data-ttu-id="608fe-142">Integer</span><span class="sxs-lookup"><span data-stu-id="608fe-142">Integer</span></span>](integer.md)     | <span data-ttu-id="608fe-143">N</span><span class="sxs-lookup"><span data-stu-id="608fe-143">N</span></span>   | <span data-ttu-id="608fe-144">O</span><span class="sxs-lookup"><span data-stu-id="608fe-144">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="608fe-145">Colonnes</span><span class="sxs-lookup"><span data-stu-id="608fe-145">Columns</span></span>

<dl> <dt>

<span data-ttu-id="608fe-146"><span id="AppId"></span><span id="appid"></span><span id="APPID"></span>AppId</span><span class="sxs-lookup"><span data-stu-id="608fe-146"><span id="AppId"></span><span id="appid"></span><span id="APPID"></span>AppId</span></span>
</dt> <dd>

<span data-ttu-id="608fe-147">La colonne AppId de la [table de classe](class-table.md) est une clé étrangère dans cette colonne de la table AppID.</span><span class="sxs-lookup"><span data-stu-id="608fe-147">The AppId column of the [Class table](class-table.md) is a foreign key into this column of the AppId table.</span></span> <span data-ttu-id="608fe-148">Cette colonne contient la valeur AppId qui sera écrite sous le CLSID et crée la clé de GUID AppId sous HKCR \\ AppID.</span><span class="sxs-lookup"><span data-stu-id="608fe-148">This column contains the AppId value that will be written under the CLSID and creates the AppId GUID key under HKCR\\AppId.</span></span>

</dd> <dt>

<span data-ttu-id="608fe-149"><span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>RemoteServerName</span><span class="sxs-lookup"><span data-stu-id="608fe-149"><span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>RemoteServerName</span></span>
</dt> <dd>

<span data-ttu-id="608fe-150">Cette colonne contient la valeur de « RemoteServerName » = <xxxx> qui sera écrite sous HKCR \\ AppID \\ {AppID} \\ .</span><span class="sxs-lookup"><span data-stu-id="608fe-150">This column contains the value of "RemoteServerName"=<xxxx> that will be written under HKCR\\AppID\\{AppID}\\ .</span></span>

</dd> <dt>

<span data-ttu-id="608fe-151"><span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>Local</span><span class="sxs-lookup"><span data-stu-id="608fe-151"><span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>LocalService</span></span>
</dt> <dd>

<span data-ttu-id="608fe-152">Cette colonne contient la valeur LocalService qui sera écrite sous HKCR \\ AppID \\ { <appid> } "LocalService" = <xxx> .</span><span class="sxs-lookup"><span data-stu-id="608fe-152">This column contains the value of LocalService that will be written under HKCR\\AppID\\{<appid>} "LocalService"=<xxx>.</span></span>

</dd> <dt>

<span data-ttu-id="608fe-153"><span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>ServiceParameters</span><span class="sxs-lookup"><span data-stu-id="608fe-153"><span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>ServiceParameters</span></span>
</dt> <dd>

<span data-ttu-id="608fe-154">Cette colonne contient la valeur de ServiceParameters qui sera écrite sous HKCR \\ AppID \\ {AppID>} "ServiceParameters".</span><span class="sxs-lookup"><span data-stu-id="608fe-154">This column contains the value of ServiceParameters that will be written under HKCR\\AppID\\{appid>} "ServiceParameters".</span></span>

</dd> <dt>

<span data-ttu-id="608fe-155"><span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="608fe-155"><span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>DllSurrogate</span></span>
</dt> <dd>

<span data-ttu-id="608fe-156">Cette colonne contient la valeur de DllSurrogate qui sera écrite sous HKCR \\ AppID \\ { <appid> } "DllSurrogate" = <xxx> .</span><span class="sxs-lookup"><span data-stu-id="608fe-156">This column contains the value of DllSurrogate that will be written under HKCR\\AppId\\{<appid>} "DllSurrogate"=<xxx>.</span></span> <span data-ttu-id="608fe-157">Si cette colonne est présente, il s’agit généralement d’une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="608fe-157">If this column is present it will typically be an empty string.</span></span>

</dd> <dt>

<span data-ttu-id="608fe-158"><span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="608fe-158"><span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>ActivateAtStorage</span></span>
</dt> <dd>

<span data-ttu-id="608fe-159">Une valeur entière différente de zéro dans ce champ amène Windows Installer à écrire HKCR \\ AppID \\ { <appid> } "ActivateAtStorage" = "Y" dans le registre.</span><span class="sxs-lookup"><span data-stu-id="608fe-159">A non-zero integer value in this field causes Windows Installer to write HKCR\\AppID\\{<appid>} "ActivateAtStorage"="Y" into the registry.</span></span> <span data-ttu-id="608fe-160">Si le champ est laissé vide ou a une valeur égale à zéro, aucune valeur ne sera écrite.</span><span class="sxs-lookup"><span data-stu-id="608fe-160">If the field is left empty, or has a value of zero, no value will be written.</span></span>

</dd> <dt>

<span data-ttu-id="608fe-161"><span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>RunAsInteractiveUser</span><span class="sxs-lookup"><span data-stu-id="608fe-161"><span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>RunAsInteractiveUser</span></span>
</dt> <dd>

<span data-ttu-id="608fe-162">Une valeur entière différente de zéro dans ce champ amène Windows Installer à écrire HKCR \\ AppID \\ {AppID>} "RunAs" = "interactive user" dans le registre.</span><span class="sxs-lookup"><span data-stu-id="608fe-162">A non-zero integer value in this field causes Windows Installer to write HKCR\\AppID\\{appid>} "RunAs"="Interactive User" into the registry.</span></span> <span data-ttu-id="608fe-163">Si le champ est laissé vide ou a une valeur égale à zéro, aucune valeur ne sera écrite.</span><span class="sxs-lookup"><span data-stu-id="608fe-163">If the field is left empty, or has a value of zero, no value will be written.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="608fe-164">Notes</span><span class="sxs-lookup"><span data-stu-id="608fe-164">Remarks</span></span>

<span data-ttu-id="608fe-165">Cette table est utilisée par l' [action RegisterClassInfo](registerclassinfo-action.md) et l' [action UnregisterClassInfo](unregisterclassinfo-action.md).</span><span class="sxs-lookup"><span data-stu-id="608fe-165">This table is used by the [RegisterClassInfo action](registerclassinfo-action.md) and [UnregisterClassInfo action](unregisterclassinfo-action.md).</span></span>

<span data-ttu-id="608fe-166">Notez que la table AppId n’a pas de colonne pour l’enregistrement d’un nom par défaut.</span><span class="sxs-lookup"><span data-stu-id="608fe-166">Note that the AppId table does not have a column for registering a Default name.</span></span> <span data-ttu-id="608fe-167">Par conséquent, dans les cas où vous devez écrire un nom convivial en tant que valeur de nom par défaut, vous devez vous inscrire à l’aide de la [table du Registre](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="608fe-167">Therefore in cases where you need to write a user friendly name as the Default name value, you must register using the [Registry table](registry-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="608fe-168">Validation</span><span class="sxs-lookup"><span data-stu-id="608fe-168">Validation</span></span>

<dl>

[<span data-ttu-id="608fe-169">ICE03</span><span class="sxs-lookup"><span data-stu-id="608fe-169">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="608fe-170">ICE06</span><span class="sxs-lookup"><span data-stu-id="608fe-170">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="608fe-171">ICE32</span><span class="sxs-lookup"><span data-stu-id="608fe-171">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="608fe-172">ICE33</span><span class="sxs-lookup"><span data-stu-id="608fe-172">ICE33</span></span>](ice33.md)  
[<span data-ttu-id="608fe-173">ICE46</span><span class="sxs-lookup"><span data-stu-id="608fe-173">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="608fe-174">ICE69</span><span class="sxs-lookup"><span data-stu-id="608fe-174">ICE69</span></span>](ice69.md)  
</dl>

 

 



