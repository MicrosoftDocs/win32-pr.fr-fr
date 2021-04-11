---
title: Configuration du plug-in du service WinRM
description: Un plug-in de Windows Remote Management (WinRM) doit être inscrit dans le catalogue WinRM pour permettre à l’infrastructure de déterminer de manière dynamique l’ensemble des plug-ins disponibles et les URI de ressource qu’ils prennent en charge.
ms.assetid: d71cd244-3f10-40e3-a756-36cdf41b9cad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60bf618d71e55c6afd28de918198725895088559
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104316734"
---
# <a name="winrm-service-plug-in-configuration"></a><span data-ttu-id="0b48f-103">Configuration du plug-in du service WinRM</span><span class="sxs-lookup"><span data-stu-id="0b48f-103">WinRM Service Plug-in Configuration</span></span>

<span data-ttu-id="0b48f-104">Un plug-in de Windows Remote Management (WinRM) doit être inscrit dans le catalogue WinRM pour permettre à l’infrastructure de déterminer de manière dynamique l’ensemble des plug-ins disponibles et les [*URI de ressource*](windows-remote-management-glossary.md) qu’ils prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="0b48f-104">A Windows Remote Management (WinRM) plug-in must be registered in the WinRM catalog to enable the infrastructure to dynamically determine the set of available plug-ins and the [*resource URIs*](windows-remote-management-glossary.md) that they support.</span></span> <span data-ttu-id="0b48f-105">Tous les [*URI de ressource*](windows-remote-management-glossary.md) pour les plug-ins WinRM doivent être conformes au format défini dans la RFC 3986 ( [https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt) ).</span><span class="sxs-lookup"><span data-stu-id="0b48f-105">All [*resource URIs*](windows-remote-management-glossary.md) for WinRM plug-ins should conform to the format that is defined in RFC 3986 ([https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt)).</span></span> <span data-ttu-id="0b48f-106">La configuration s’effectue par le biais du service WinRM principal.</span><span class="sxs-lookup"><span data-stu-id="0b48f-106">Configuration is done through the main WinRM service.</span></span>

<span data-ttu-id="0b48f-107">La commande suivante inscrit une configuration de plug-in auprès du service WinRM :</span><span class="sxs-lookup"><span data-stu-id="0b48f-107">The following command registers a plug-in configuration with the WinRM service:</span></span>

```console
winrm create http://schemas.microsoft.com/wbem/wsman/1/config/plugin?name=MyPlugIn -file:myplugin.xml
```

> [!NOTE]
> <span data-ttu-id="0b48f-108">Le service WinRM doit être redémarré pour exposer les plug-ins nouvellement inscrits.</span><span class="sxs-lookup"><span data-stu-id="0b48f-108">The WinRM service needs to be restarted to expose the newly registered plug-ins.</span></span>

<span data-ttu-id="0b48f-109">La configuration du plug-in est spécifiée au format XML.</span><span class="sxs-lookup"><span data-stu-id="0b48f-109">Plug-in configuration is specified in XML.</span></span> <span data-ttu-id="0b48f-110">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="0b48f-110">The following is an example.</span></span>

```XML
<PlugInConfiguration xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
                     Name="MyPlugIn"
                     Filename="%systemroot%\system32\myplugin.dll" 
                     SDKVersion="1"
                     XmlRenderingType="text"
                     Architecture="64"
                     Enabled="true">

 <InitializationParameters>
  <Param Name="myParam1" Value="myValue1"/>
  <Param Name="myParam2" Value="myValue2"/>
 </InitializationParameters>

 <Resources>
  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri1" SupportsOptions="true" ExactMatch="false">
   <Capability Type="Get" SupportsFragment="true"/>
   <Capability Type="Put" SupportsFragment="true"/>
   <Capability Type="Create"/>
   <Capability Type="Delete"/>
   <Capability Type="Invoke"/>
   <Capability Type="Enumerate" SupportsFiltering="true"/>
  </Resource>

  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri2" SupportsOptions="false" ExactMatch="true">
   <Security Uri="https://schemas.MyCompany.com/MyUri2" Sddl="O:NSG:BAD:P(A;;GA;;;BA)"/>
   <Security Uri="https://schemas.MyCompany.com/MyUri2/MoreSpecific" Sddl="O:NSG:BAD:P(A;;GR;;;BA)" ExactMatch="true"/>
   <Capability Type="Shell"/>
  </Resource>
 </Resources>
</PlugInConfiguration>
```



<span data-ttu-id="0b48f-111">La liste suivante décrit les éléments XML plus en détail et est suivie du schéma de configuration spécifié en tant que XSD.</span><span class="sxs-lookup"><span data-stu-id="0b48f-111">The following list describes the XML elements in more detail and is followed by the configuration schema specified as an XSD.</span></span>

<dl> <dt>

<span data-ttu-id="0b48f-112"><span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**PlugInConfiguration** / **OperationsConfiguration**</span><span class="sxs-lookup"><span data-stu-id="0b48f-112"><span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**PlugInConfiguration**/**OperationsConfiguration**</span></span>
</dt> <dd>

<span data-ttu-id="0b48f-113">Spécifie le nom de fichier du plug-in d’opérations.</span><span class="sxs-lookup"><span data-stu-id="0b48f-113">Specifies the file name of the operations plug-in.</span></span> <span data-ttu-id="0b48f-114">Toutes les variables d’environnement qui sont placées dans cette entrée sont développées dans le contexte des utilisateurs lorsqu’une demande arrive.</span><span class="sxs-lookup"><span data-stu-id="0b48f-114">Any environment variables that are put in this entry will be expanded in the users' context when a request comes in.</span></span> <span data-ttu-id="0b48f-115">Chaque utilisateur peut avoir une version différente de la même variable d’environnement, afin que chaque utilisateur puisse se retrouver avec un autre plug-in.</span><span class="sxs-lookup"><span data-stu-id="0b48f-115">Each user could have a different version of the same environment variable, so each user could end up with a different plug-in.</span></span> <span data-ttu-id="0b48f-116">Cette entrée ne peut pas être vide et doit pointer vers un plug-in valide.</span><span class="sxs-lookup"><span data-stu-id="0b48f-116">This entry cannot be blank and must point to a valid plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="0b48f-117"><span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**PlugInConfiguration** / **Nom**</span><span class="sxs-lookup"><span data-stu-id="0b48f-117"><span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**PlugInConfiguration**/**Name**</span></span>
</dt> <dd>

<span data-ttu-id="0b48f-118">Spécifie le nom complet à utiliser pour le plug-in.</span><span class="sxs-lookup"><span data-stu-id="0b48f-118">Specifies the display name to use for the plug-in.</span></span> <span data-ttu-id="0b48f-119">Si une erreur est retournée par le plug-in, ce nom est placé dans le code XML d’erreur renvoyé à l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="0b48f-119">If an error is returned from the plug-in, this name will be put into the error XML that is returned to the client application.</span></span> <span data-ttu-id="0b48f-120">Le nom n'est pas spécifique aux paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="0b48f-120">The name is not locale specific.</span></span>

</dd> <dt>

<span data-ttu-id="0b48f-121"><span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**PlugInConfiguration** / **Architecture**</span><span class="sxs-lookup"><span data-stu-id="0b48f-121"><span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**PlugInConfiguration**/**Architecture**</span></span>
</dt> <dd>

<span data-ttu-id="0b48f-122">Spécifie si le plug-in d’opérations est 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0b48f-122">Specifies whether the operations plug-in is 32-bit or 64-bit.</span></span> <span data-ttu-id="0b48f-123">Si cet élément n’est pas spécifié, la valeur par défaut est « 32 » sur les systèmes x86 et « 64 » sur les systèmes 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0b48f-123">If this element is not specified, the value will default to "32" on x86 systems and to "64" on 64-bit systems.</span></span> <span data-ttu-id="0b48f-124">Pour les systèmes x86, la seule valeur valide est « 32 ».</span><span class="sxs-lookup"><span data-stu-id="0b48f-124">For x86 systems, the only valid value is "32".</span></span> <span data-ttu-id="0b48f-125">Si la valeur est « 32 » sur un système 64 bits, la redirection WOW64 doit être prise en compte lors de l’entrée des informations de **nom de fichier** .</span><span class="sxs-lookup"><span data-stu-id="0b48f-125">If the value is "32" on an 64-bit system, wow64 redirection needs to be taken into account when entering the **Filename** information.</span></span> <span data-ttu-id="0b48f-126">Le système de fichiers sous-jacent utilise la redirection WOW64 pour traduire system32 en SysWOW64.</span><span class="sxs-lookup"><span data-stu-id="0b48f-126">The underlying file system will use wow64 redirection to translate system32 to syswow64.</span></span> <span data-ttu-id="0b48f-127">Par exemple, si le **nom de fichier** est « % windir% \\ system32 \\myplugin.dll » et que l' **architecture** est « 32 », le fichier de plug-in réel se trouve dans « % windir% \\ SysWOW64 \\myplugin.dll ».</span><span class="sxs-lookup"><span data-stu-id="0b48f-127">For example, if **Filename** is "%windir%\\system32\\myplugin.dll" and **Architecture** is "32", the actual plug-in file is located at "%windir%\\syswow64\\myplugin.dll".</span></span>

</dd> <dt>

<span data-ttu-id="0b48f-128"><span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**PlugInConfiguration** / **XmlRenderingType**</span><span class="sxs-lookup"><span data-stu-id="0b48f-128"><span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**PlugInConfiguration**/**XmlRenderingType**</span></span>
</dt> <dd>

<span data-ttu-id="0b48f-129">Configure le format dans lequel le code XML est transmis aux plug-ins via l’objet de [**\_ données WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) .</span><span class="sxs-lookup"><span data-stu-id="0b48f-129">Configures the format in which XML is passed to plug-ins through the [**WSMAN\_DATA**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) object.</span></span> <span data-ttu-id="0b48f-130">Les types suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="0b48f-130">The following types are available:</span></span>

<dl> <dt>

<span data-ttu-id="0b48f-131"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Financière</span><span class="sxs-lookup"><span data-stu-id="0b48f-131"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="0b48f-132">Les données XML entrantes sont contenues dans une \_ structure de type de données WSMan \_ \_ , qui représente le XML sous la forme d’une mémoire tampon **PCWSTR** .</span><span class="sxs-lookup"><span data-stu-id="0b48f-132">Incoming XML data is contained in a WSMAN\_DATA\_TYPE\_TEXT structure, which represents the XML as a **PCWSTR** memory buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0b48f-133"><span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>Lecteurs</span><span class="sxs-lookup"><span data-stu-id="0b48f-133"><span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>XMLReader</span></span>
</dt> <dd>

<span data-ttu-id="0b48f-134">Les données XML entrantes sont contenues dans un \_ type de données WSMan \_ structure de \_ \_ lecteur WS XML \_ , qui représente le XML sous la forme d’un objet **XmlReader** , qui est défini dans le fichier d’en-tête WebServices. h.</span><span class="sxs-lookup"><span data-stu-id="0b48f-134">Incoming XML data is contained in a WSMAN\_DATA\_TYPE\_WS\_XML\_READER structure, which represents the XML as an **XmlReader** object, which is defined in the WebServices.h header file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0b48f-135"><span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**PlugInConfiguration** / **InitializationXml**</span><span class="sxs-lookup"><span data-stu-id="0b48f-135"><span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**PlugInConfiguration**/**InitializationXml**</span></span>
</dt> <dd>

<span data-ttu-id="0b48f-136">Ce nœud est facultatif et permet à un plug-in de configurer du code XML supplémentaire qui sera transmis à la méthode [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup).</span><span class="sxs-lookup"><span data-stu-id="0b48f-136">This node is optional and allows a plug-in to configure extra XML that will be passed in to the [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)method.</span></span> <span data-ttu-id="0b48f-137">La plupart des plug-ins n’ont pas besoin de ces informations supplémentaires, mais si un plug-in doit être utilisé dans plusieurs scénarios qui nécessitent une sémantique d’exécution différente, ce code XML offre au plug-in la flexibilité nécessaire pour effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="0b48f-137">Most plug-ins will not need this extra information, but if a plug-in needs to be used under more than one scenario that requires different run-time semantics, this XML will give the plug-in the flexibility to do this.</span></span>

</dd> <dt>

<span data-ttu-id="0b48f-138"><span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**PlugInConfiguration** / **Ressources**</span><span class="sxs-lookup"><span data-stu-id="0b48f-138"><span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**PlugInConfiguration**/**Resources**</span></span>
</dt> <dd>

<span data-ttu-id="0b48f-139">Spécifie la liste des [*URI de ressource*](windows-remote-management-glossary.md)que ce plug-in prend en charge.</span><span class="sxs-lookup"><span data-stu-id="0b48f-139">Specifies a list of [*resource URIs*](windows-remote-management-glossary.md)that this plug-in supports.</span></span> <span data-ttu-id="0b48f-140">Au moins une entrée **resourceuri** doit être spécifiée ; dans le cas contraire, le code XML sera rejeté.</span><span class="sxs-lookup"><span data-stu-id="0b48f-140">At least one **ResourceUri** entry must be specified; otherwise, the XML will be rejected.</span></span>

</dd> <dt>

<span data-ttu-id="0b48f-141"><span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**PlugInConfiguration** / **Ressources** / **Ressource**</span><span class="sxs-lookup"><span data-stu-id="0b48f-141"><span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**PlugInConfiguration**/**Resources**/**Resource**</span></span>
</dt> <dd>

<span data-ttu-id="0b48f-142">Représente une configuration d' [*URI de ressource*](windows-remote-management-glossary.md)unique.</span><span class="sxs-lookup"><span data-stu-id="0b48f-142">Represents a single [*resource URI*](windows-remote-management-glossary.md)configuration.</span></span>

> [!Note]  
> <span data-ttu-id="0b48f-143">L’attribut **SupportsOptions** peut avoir la valeur false.</span><span class="sxs-lookup"><span data-stu-id="0b48f-143">The **SupportsOptions** attribute can be set to false.</span></span> <span data-ttu-id="0b48f-144">Si **SupportsOptions** a la valeur false, cet attribut n’est pas répertorié lorsque la ressource est énumérée.</span><span class="sxs-lookup"><span data-stu-id="0b48f-144">If **SupportsOptions** is set to false, this attribute is not listed when the resource is enumerated.</span></span>

 

</dd> <dt>

<span data-ttu-id="0b48f-145"><span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**PlugInConfiguration** / **Ressources** / **Ressource** / **Resourceuri**</span><span class="sxs-lookup"><span data-stu-id="0b48f-145"><span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**PlugInConfiguration**/**Resources**/**Resource**/**ResourceUri**</span></span>
</dt> <dd>

<span data-ttu-id="0b48f-146">Spécifie un [*URI de ressource*](windows-remote-management-glossary.md) unique complet ou une chaîne de correspondance partielle basée sur l’attribut **ExactMatch** .</span><span class="sxs-lookup"><span data-stu-id="0b48f-146">Specifies a single [*resource URI*](windows-remote-management-glossary.md) either in full or as a partial match string based on the **ExactMatch** attribute.</span></span> <span data-ttu-id="0b48f-147">Si **ExactMatch** n’est pas présent, la valeur par défaut est **false**, ce qui signifie que le processeur SOAP WinRM effectue une correspondance partielle avec le début de l' *URI de ressource* et, s’il existe une correspondance, la passe au plug-in.</span><span class="sxs-lookup"><span data-stu-id="0b48f-147">If **ExactMatch** is not present, it defaults to **False**, which means the WinRM SOAP processor will do a partial match to the start of the *resource URI* and, if there is a match, pass it to the plug-in.</span></span> <span data-ttu-id="0b48f-148">L’attribut **SupportsOptions** peut être spécifié si des options sont autorisées pour cet *URI de ressource* .</span><span class="sxs-lookup"><span data-stu-id="0b48f-148">The **SupportsOptions** attribute can be specified if this *resource URI* is allowed to have any options passed in.</span></span> <span data-ttu-id="0b48f-149">Par défaut, aucune option n’est prise en charge et, si elle est présente dans la demande du client, une erreur est retournée.</span><span class="sxs-lookup"><span data-stu-id="0b48f-149">By default, no options are supported, and if any are present in the client request, an error will be returned.</span></span> <span data-ttu-id="0b48f-150">Si les options sont prises en charge par le plug-in, il est important que le plug-in retourne l’erreur correcte si le plug-in n’est pas compris lorsque l’indicateur **MustUnderstand** a la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="0b48f-150">If options are supported by the plug-in, it is important that the plug-in returns the correct error if an option is present that the plug-in does not understand when the **mustUnderstand** flag is set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="0b48f-151"><span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**PlugInConfiguration** / **Ressources** / **Ressource** / **Fonctionnalité**</span><span class="sxs-lookup"><span data-stu-id="0b48f-151"><span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**PlugInConfiguration**/**Resources**/**Resource**/**Capability**</span></span>
</dt> <dd>

<span data-ttu-id="0b48f-152">Spécifie une fonctionnalité disponible sur cet [*URI de ressource*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="0b48f-152">Specifies a capability that is available on this [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="0b48f-153">Il y aura une entrée pour chaque type d’opération qu’elle prend en charge.</span><span class="sxs-lookup"><span data-stu-id="0b48f-153">There will be one entry for each type of operation that it supports.</span></span> <span data-ttu-id="0b48f-154">Les options suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="0b48f-154">The following options are available:</span></span>

<dl> <dt>

<span data-ttu-id="0b48f-155"><span id="Get"></span><span id="get"></span><span id="GET"></span>Télécharger</span><span class="sxs-lookup"><span data-stu-id="0b48f-155"><span id="Get"></span><span id="get"></span><span id="GET"></span>Get</span></span>
</dt> <dd>

<span data-ttu-id="0b48f-156">Les opérations d’extraction sont prises en charge sur l' [*URI de ressource*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="0b48f-156">Get operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="0b48f-157">L’attribut **SupportFragment** est utilisé si l’opération d’extraction prend en charge le concept.</span><span class="sxs-lookup"><span data-stu-id="0b48f-157">The **SupportFragment** attribute is used if the get operation supports the concept.</span></span> <span data-ttu-id="0b48f-158">L’attribut **SupportFiltering** n’est pas valide et doit avoir la valeur false.</span><span class="sxs-lookup"><span data-stu-id="0b48f-158">The **SupportFiltering** attribute is not valid and should be set to false.</span></span> <span data-ttu-id="0b48f-159">Cette fonctionnalité n’est pas valide pour un *URI de ressource* si les opérations de l’interpréteur de commandes sont également prises en charge.</span><span class="sxs-lookup"><span data-stu-id="0b48f-159">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="0b48f-160"><span id="Put"></span><span id="put"></span><span id="PUT"></span>Posé</span><span class="sxs-lookup"><span data-stu-id="0b48f-160"><span id="Put"></span><span id="put"></span><span id="PUT"></span>Put</span></span>
</dt> <dd>

<span data-ttu-id="0b48f-161">Les opérations put sont prises en charge sur l' [*URI de ressource*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="0b48f-161">Put operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="0b48f-162">L’attribut **SupportFragment** est utilisé si l’opération put prend en charge le concept.</span><span class="sxs-lookup"><span data-stu-id="0b48f-162">The **SupportFragment** attribute is used if the put operation supports the concept.</span></span> <span data-ttu-id="0b48f-163">L’attribut **SupportFiltering** n’est pas valide et doit avoir la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="0b48f-163">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="0b48f-164">Cette fonctionnalité n’est pas valide pour un *URI de ressource* si les opérations de l’interpréteur de commandes sont également prises en charge.</span><span class="sxs-lookup"><span data-stu-id="0b48f-164">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="0b48f-165"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>Créés</span><span class="sxs-lookup"><span data-stu-id="0b48f-165"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>Create</span></span>
</dt> <dd>

<span data-ttu-id="0b48f-166">Les opérations Create sont prises en charge sur l' [*URI de ressource*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="0b48f-166">Create operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="0b48f-167">L’attribut **SupportFragment** est utilisé si l’opération de création prend en charge le concept.</span><span class="sxs-lookup"><span data-stu-id="0b48f-167">The **SupportFragment** attribute is used if the create operation supports the concept.</span></span> <span data-ttu-id="0b48f-168">L’attribut **SupportFiltering** n’est pas valide et doit avoir la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="0b48f-168">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="0b48f-169">Cette fonctionnalité n’est pas valide pour un *URI de ressource* si les opérations de l’interpréteur de commandes sont également prises en charge.</span><span class="sxs-lookup"><span data-stu-id="0b48f-169">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="0b48f-170"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>Supprimer</span><span class="sxs-lookup"><span data-stu-id="0b48f-170"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>Delete</span></span>
</dt> <dd>

<span data-ttu-id="0b48f-171">Les opérations de suppression sont prises en charge sur l' [*URI de ressource*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="0b48f-171">Delete operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="0b48f-172">L’attribut **SupportFragment** est utilisé si l’opération de suppression prend en charge le concept.</span><span class="sxs-lookup"><span data-stu-id="0b48f-172">The **SupportFragment** attribute is used if the delete operation supports the concept.</span></span> <span data-ttu-id="0b48f-173">L’attribut **SupportFiltering** n’est pas valide et doit avoir la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="0b48f-173">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="0b48f-174">Cette fonctionnalité n’est pas valide pour un *URI de ressource* si les opérations de l’interpréteur de commandes sont également prises en charge.</span><span class="sxs-lookup"><span data-stu-id="0b48f-174">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="0b48f-175"><span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>Déclenché</span><span class="sxs-lookup"><span data-stu-id="0b48f-175"><span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>Invoke</span></span>
</dt> <dd>

<span data-ttu-id="0b48f-176">Les opérations d’appel sont prises en charge sur l' [*URI de ressource*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="0b48f-176">Invoke operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="0b48f-177">L’attribut **SupportFragment** n’est pas pris en charge pour les opérations d’appel et doit avoir la valeur false.</span><span class="sxs-lookup"><span data-stu-id="0b48f-177">The **SupportFragment** attribute is not supported for invoke operations and should be set to false.</span></span> <span data-ttu-id="0b48f-178">L’attribut **SupportFiltering** n’est pas valide et doit avoir la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="0b48f-178">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="0b48f-179">Cette fonctionnalité n’est pas valide pour un *URI de ressource* si les opérations de l’interpréteur de commandes sont également prises en charge.</span><span class="sxs-lookup"><span data-stu-id="0b48f-179">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="0b48f-180"><span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>Énumérer</span><span class="sxs-lookup"><span data-stu-id="0b48f-180"><span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>Enumerate</span></span>
</dt> <dd>

<span data-ttu-id="0b48f-181">Les opérations d’énumération sont prises en charge sur l' [*URI de ressource*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="0b48f-181">Enumerate operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="0b48f-182">L’attribut **SupportFragment** n’est pas pris en charge pour les opérations d’énumération et doit avoir la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="0b48f-182">The **SupportFragment** attribute is not supported for enumerate operations and should be set to **False**.</span></span> <span data-ttu-id="0b48f-183">L’attribut **SupportFiltering** est valide, et si le plug-in prend en charge le filtrage, cet attribut doit avoir la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="0b48f-183">The **SupportFiltering** attribute is valid, and if the plug-in supports filtering this attribute should be set to **True**.</span></span> <span data-ttu-id="0b48f-184">Cette fonctionnalité n’est pas valide pour un *URI de ressource* si les opérations de l’interpréteur de commandes sont également prises en charge.</span><span class="sxs-lookup"><span data-stu-id="0b48f-184">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="0b48f-185"><span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>Inscrivez</span><span class="sxs-lookup"><span data-stu-id="0b48f-185"><span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>Subscribe</span></span>
</dt> <dd>

<span data-ttu-id="0b48f-186">Les opérations d’abonnement sont prises en charge sur l' [*URI de ressource*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="0b48f-186">Subscribe operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="0b48f-187">L’attribut **SupportFragment** n’est pas pris en charge pour les opérations subscribe et doit être défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="0b48f-187">The **SupportFragment** attribute is not supported for subscribe operations and should be set to **False**.</span></span> <span data-ttu-id="0b48f-188">L’attribut **SupportFiltering** n’est pas valide et doit avoir la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="0b48f-188">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="0b48f-189">Cette fonctionnalité n’est pas valide pour un *URI de ressource* si les opérations de l’interpréteur de commandes sont également prises en charge.</span><span class="sxs-lookup"><span data-stu-id="0b48f-189">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="0b48f-190"><span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>Shell</span><span class="sxs-lookup"><span data-stu-id="0b48f-190"><span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>Shell</span></span>
</dt> <dd>

<span data-ttu-id="0b48f-191">Les opérations de Shell sont prises en charge sur l' [*URI de ressource*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="0b48f-191">Shell operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="0b48f-192">L’attribut **SupportFragment** n’est pas pris en charge pour les opérations de Shell et doit avoir la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="0b48f-192">The **SupportFragment** attribute is not supported for shell operations and should be set to **False**.</span></span> <span data-ttu-id="0b48f-193">L’attribut **SupportFiltering** n’est pas valide et doit avoir la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="0b48f-193">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="0b48f-194">Cette fonctionnalité n’est pas valide pour un *URI de ressource* si une autre fonction d’opération est également prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0b48f-194">This capability is not valid for a *resource URI* if any other operation capability is also supported.</span></span> <span data-ttu-id="0b48f-195">Si une fonctionnalité de l’interpréteur de commandes est configurée pour un *URI de ressource*, les opérations obtenir, placer, créer, supprimer, appeler et énumérer sont traitées en interne dans le service WinRM pour gérer les interpréteurs de commandes.</span><span class="sxs-lookup"><span data-stu-id="0b48f-195">If a shell operation capability is configured for a *resource URI*, then get, put, create, delete, invoke, and enumerate operations are processed internally within the WinRm service to manage shells.</span></span> <span data-ttu-id="0b48f-196">Par conséquent, le plug-in ne peut pas traiter les opérations elles-mêmes.</span><span class="sxs-lookup"><span data-stu-id="0b48f-196">As a result, the plug-in cannot deal with the operations itself.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0b48f-197"><span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**PlugInConfiguration** / **Ressources** / **Ressource** / **Sécurité**</span><span class="sxs-lookup"><span data-stu-id="0b48f-197"><span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**PlugInConfiguration**/**Resources**/**Resource**/**Security**</span></span>
</dt> <dd>

<span data-ttu-id="0b48f-198">Cet élément définit le descripteur de sécurité (via l’attribut **SDDL** ) qui doit être appliqué pour déterminer l’accès à un [*URI de ressource*](windows-remote-management-glossary.md) particulier (via l’attribut **URI** ).</span><span class="sxs-lookup"><span data-stu-id="0b48f-198">This element defines the security descriptor (via the **Sddl** attribute) that should be applied to determine access to a particular [*resource URI*](windows-remote-management-glossary.md) (via the **Uri** attribute).</span></span> <span data-ttu-id="0b48f-199">Si **ExactMatch** n’est pas présent, l’élément de **sécurité** prend par défaut la **valeur false**, ce qui signifie que le **SDDL** s’applique à tous les *URI de ressource* qui partagent l' **URI** en tant que préfixe.</span><span class="sxs-lookup"><span data-stu-id="0b48f-199">If **ExactMatch** is not present, the **Security** element defaults to **False**, which means that the **Sddl** applies to all *resource URIs* that share **Uri** as a prefix.</span></span> <span data-ttu-id="0b48f-200">Si **ExactMatch** a la valeur true, le **SDDL** s’applique uniquement à l' **URI** exact spécifié.</span><span class="sxs-lookup"><span data-stu-id="0b48f-200">If **ExactMatch** is set to true, the **Sddl** applies only to the exact **Uri** specified.</span></span> <span data-ttu-id="0b48f-201">S’il existe plusieurs entrées de **sécurité** qui peuvent s’appliquer à un *URI de ressource* particulier, la correspondance de préfixe la plus longue est utilisée pour déterminer le **SDDL** approprié.</span><span class="sxs-lookup"><span data-stu-id="0b48f-201">If there are multiple **Security** entries that could apply to a particular *resource URIs*, the longest-prefix match is used to determine the appropriate **Sddl**.</span></span> <span data-ttu-id="0b48f-202">En raison de la correspondance de préfixe la plus longue, si une entrée d' **URI** de correspondance exacte existe, elle est toujours choisie comme l’élément de sécurité approprié.</span><span class="sxs-lookup"><span data-stu-id="0b48f-202">As a result of the longest-prefix match, if an exact-match **Uri** entry exists, it will always be chosen as the appropriate Security element.</span></span>

</dd> </dl>

<span data-ttu-id="0b48f-203">Voici le schéma de configuration de plug-in spécifié en tant que XSD.</span><span class="sxs-lookup"><span data-stu-id="0b48f-203">The following is the plug-in configuration schema specified as an XSD.</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8"?>
<xs:schema attributeFormDefault="unqualified" 
           elementFormDefault="qualified" 
           targetNamespace="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns:xs="https://www.w3.org/2001/XMLSchema">
 <xs:element name="PlugInConfiguration">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="InitializationParameters" minOccurs="0" maxOccurs="1">
     <xs:complexType>
      <xs:sequence>
       <xs:element name="Param">
        <xs:complexType>
         <xs:sequence></xs:sequence>
         <xs:attribute name="Name" type="xs:string"/>
         <xs:attribute name="Value" type="xs:string"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
    <xs:element name="Resources">
     <xs:complexType>
      <xs:sequence>
       <xs:element minOccurs="1" maxOccurs="unbounded" name="Resource">
        <xs:complexType>
         <xs:sequence>
          <xs:element name="Capability" minOccurs="1" maxOccurs="unbounded">
           <xs:complexType>
            <xs:simpleContent>
             <xs:extension base="ResourceCapabilityType">
              <xs:attribute name="SupportsFragment" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="SupportsFiltering" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="Type" type="ResourceCapabilityType"/>
             </xs:extension>
            </xs:simpleContent>
           </xs:complexType>
          </xs:element>
          <xs:element name="Security" minOccurs="0" maxOccurs="unbounded">
           <xs:complexType>
            <xs:sequence></xs:sequence>
            <xs:attribute name="Uri" type="xs:string"/>
            <xs:attribute name="Sddl" type="xs:string"/>
            <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
           </xs:complexType>
          </xs:element>
         </xs:sequence>
         <xs:attribute name="ResourceUri" type="xs:string"/>
         <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
         <xs:attribute name="SupportOptions" type="xs:boolean" use="optional" default="false"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
   </xs:sequence>
   <xs:attribute name="Filename" type="xs:token"/>
   <xs:attribute name="SDKVersion" type="xs:unsignedInt"/>
   <xs:attribute name="Name" type="xs:string"/>
   <xs:attribute name="XmlRenderingType" type="XmlRenderingTypeType" use="optional" default="text"/>
   <!--Architecture will default to 32 on x86 systems; 64 on 64-bit systems.-->
   <xs:attribute name="Architecture" type="ArchitectureType" use="optional" default="32"/>
  </xs:complexType>
 </xs:element>
 <xs:simpleType name="ResourceCapabilityType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="Get"/>
   <xs:enumeration value="Put"/>
   <xs:enumeration value="Create"/>
   <xs:enumeration value="Delete"/>
   <xs:enumeration value="Invoke"/>
   <xs:enumeration value="Enumerate"/>
   <xs:enumeration value="Subscribe"/>
   <xs:enumeration value="Shell"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="XmlRenderingTypeType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="text"/>
   <xs:enumeration value="XmlReader"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="ArchitectureType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="32"/>
   <xs:enumeration value="64"/>
  </xs:restriction>
 </xs:simpleType>
</xs:schema>
```

 

 




