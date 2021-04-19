---
title: Implémentation du comportement de l’appareil
description: Le comportement d’un appareil est défini par les services qu’il expose.
ms.assetid: 5b352870-6de1-42f2-a178-ed7036b7afc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb702adf3ccb0f21bc71f08e98427cca15495f3b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106525813"
---
# <a name="implementing-device-behavior"></a><span data-ttu-id="aba2b-103">Implémentation du comportement de l’appareil</span><span class="sxs-lookup"><span data-stu-id="aba2b-103">Implementing Device Behavior</span></span>

<span data-ttu-id="aba2b-104">Le comportement d’un appareil est défini par les services qu’il expose.</span><span class="sxs-lookup"><span data-stu-id="aba2b-104">The behavior of a device is defined by the services it exposes.</span></span> <span data-ttu-id="aba2b-105">Chaque service a une description de service qui répertorie ses actions et ses variables d’État.</span><span class="sxs-lookup"><span data-stu-id="aba2b-105">Each service has a service description that lists its actions and state variables.</span></span> <span data-ttu-id="aba2b-106">Pris ensemble, ces descriptions de service composent l’interface de service, qui définit la façon dont un point de contrôle peut interagir avec un service.</span><span class="sxs-lookup"><span data-stu-id="aba2b-106">Taken together, these service descriptions make up the service interface, which defines the way in which a control point can interact with a service.</span></span> <span data-ttu-id="aba2b-107">Chaque service doit avoir au moins une action.</span><span class="sxs-lookup"><span data-stu-id="aba2b-107">Each service must have at least one action.</span></span>

<span data-ttu-id="aba2b-108">Pour implémenter un service, un appareil hébergé doit fournir un objet COM (Component Object Model) qui expose l’interface pour le service.</span><span class="sxs-lookup"><span data-stu-id="aba2b-108">To implement a service, a hosted device must provide a Component Object Model (COM) object that exposes the interface for the service.</span></span> <span data-ttu-id="aba2b-109">Dans la description du service, les interfaces de service sont spécifiées dans le langage de modèles UPnP (UTL); Toutefois, les interfaces d’objets COM sont généralement spécifiées dans le langage IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="aba2b-109">In the service description, the service interfaces are specified in UPnP Template Language (UTL); however, COM object interfaces typically are specified in Interface Definition Language (IDL).</span></span> <span data-ttu-id="aba2b-110">Vous pouvez également spécifier l’interface COM dans une bibliothèque de types ou un fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="aba2b-110">You can also specify the COM interface in a type library or header file.</span></span> <span data-ttu-id="aba2b-111">Le kit de développement logiciel (SDK) de la plateforme comprend l’outil Utl2idl, qui traduit une description de service dans UTL en une interface COM dans IDL.</span><span class="sxs-lookup"><span data-stu-id="aba2b-111">The Platform Software Development Kit (SDK) includes the Utl2idl tool, which translates a service description in UTL to a COM interface in IDL.</span></span>

<span data-ttu-id="aba2b-112">Les exemples suivants illustrent ce processus de conversion.</span><span class="sxs-lookup"><span data-stu-id="aba2b-112">The following samples illustrate this conversion process.</span></span> <span data-ttu-id="aba2b-113">La description du service est fournie par le développeur de l’appareil et est écrite en UTL.</span><span class="sxs-lookup"><span data-stu-id="aba2b-113">The service description is provided by the device developer and is written in UTL.</span></span>

``` syntax
<?xml version="1.0" ?> 
  <scpd xmlns="urn:schemas-upnp-org:service-1-0">

    <specVersion>
      <major>1</major> 
      <minor>0</minor> 
    </specVersion>

    <serviceStateTable>
      <stateVariable>
        <name>Power</name> 
        <dataType>Boolean</dataType> 
        <defaultValue>0</defaultValue> 
      </stateVariable>

      <stateVariable>
        <name>Level</name> 
        <dataType>i4</dataType> 
        <allowedValueRange>
          <minimum>0</minimum> 
            <maximum>10</maximum> 
            <step>1</step> 
        </allowedValueRange>
        <defaultValue>0</defaultValue> 
      </stateVariable>

      <stateVariable>
        <name>State</name> 
        <dataType>string</dataType> 
        <allowedValueList>
          <allowedValue>ON</allowedValue> 
          <allowedValue>OFF</allowedValue> 
          <allowedValue>DIMMED</allowedValue> 
        </allowedValueList>
        <defaultValue>OFF</defaultValue> 
      </stateVariable>
    </serviceStateTable>

    <actionList>
      <action>
        <name>PowerOn</name> 
      </action>

      <action>
        <name>PowerOff</name> 
      </action>

      <action>
        <name>SetLevel</name> 
        <argumentList>
          <argument>
            <name>NewLevel</name> 
            <relatedStateVariable>Level</relatedStateVariable> 
            <direction>in</direction> 
          </argument>
          <argument>
            <name>NewState</name> 
            <relatedStateVariable>State</relatedStateVariable> 
            <direction>out</direction> 
          </argument>
        </argumentList>
      </action>

      <action>
        <name>IncreaseLevel</name> 
      </action>

      <action>
        <name>DecreaseLevel</name> 
      </action>
    </actionList>
</scpd>
```

<span data-ttu-id="aba2b-114">L’étape suivante consiste à exécuter l’outil Utl2idl.</span><span class="sxs-lookup"><span data-stu-id="aba2b-114">The next step is to run the Utl2idl tool.</span></span> <span data-ttu-id="aba2b-115">Il produit le fichier IDL qui contient l’interface COM.</span><span class="sxs-lookup"><span data-stu-id="aba2b-115">It produces the IDL file that contains the COM interface.</span></span> <span data-ttu-id="aba2b-116">Pour plus d’informations sur les fichiers IDL et le mot clé **interface** , consultez [fichier de définition d’interface (IDL)](/windows/desktop/Midl/interface-definition-idl-file) et [**interface**](/windows/desktop/Midl/interface) dans la référence MIDL.</span><span class="sxs-lookup"><span data-stu-id="aba2b-116">For more information about IDL files and the **interface** keyword, see [Interface Definition (IDL) File](/windows/desktop/Midl/interface-definition-idl-file) and [**interface**](/windows/desktop/Midl/interface) in the MIDL reference.</span></span>

``` syntax
#include <windows.h>
typedef [v1_enum] enum SCPD_DISPIDS
{
     DISPID_POWER = 1,
     DISPID_LEVEL,
     DISPID_STATE,
     DISPID_POWERON,
     DISPID_POWEROFF,
     DISPID_SETLEVEL,
     DISPID_INCREASELEVEL,
     DISPID_DECREASELEVEL
} SCPD_DISPIDS;

[
     uuid(68369839-960d-4c8c-8d0d-c319c69e73be),
     oleautomation,
     pointer_default(unique)
]
interface IUPnPService_scpd : IUnknown 
{
     [propget, id(DISPID_POWER), helpstring("Property Power")]
     HRESULT Power(
          [out, retval] VARIANT_BOOL *pPower);

     [propget, id(DISPID_LEVEL), helpstring("Property Level")]
     HRESULT Level(
          [out, retval] long *pLevel);

     [propget, id(DISPID_STATE), helpstring("Property State")]
     HRESULT State(
          [out, retval] BSTR *pState);

     [ id(DISPID_POWERON), helpstring("Method PowerOn")]
     HRESULT PowerOn();

     [ id(DISPID_POWEROFF), helpstring("Method PowerOff")]
     HRESULT PowerOff();

     [ id(DISPID_SETLEVEL), helpstring("Method SetLevel")]
     HRESULT SetLevel(
          [in] long NewLevel,
          [in, out] BSTR *pNewState;
                                
     [ id(DISPID_INCREASELEVEL), helpstring("Method IncreaseLevel")]
     HRESULT IncreaseLevel();

     [ id(DISPID_DECREASELEVEL), helpstring("Method DecreaseLevel")]
     HRESULT DecreaseLevel();
};
```

> [!Note]
> <span data-ttu-id="aba2b-117">La valeur de retour est le \[ premier \] paramètre de sortie dans la liste d’arguments dans la description de service ; toutefois, elle est répertoriée en tant que dernier paramètre après translation.</span><span class="sxs-lookup"><span data-stu-id="aba2b-117">The return value is the first \[out\] parameter in the list of arguments in the service description; however, it is listed as the last parameter after translation.</span></span>
> 
> <span data-ttu-id="aba2b-118">Tous les autres paramètres restent dans le même ordre.</span><span class="sxs-lookup"><span data-stu-id="aba2b-118">All other parameters remain in the same order.</span></span>

 

<span data-ttu-id="aba2b-119">Pour fournir les fonctionnalités du service, implémentez cette interface COM.</span><span class="sxs-lookup"><span data-stu-id="aba2b-119">To provide the functionality of the service, implement this COM interface.</span></span>

## <a name="obtaining-information-about-an-endpoint"></a><span data-ttu-id="aba2b-120">Obtention d’informations sur un point de terminaison</span><span class="sxs-lookup"><span data-stu-id="aba2b-120">Obtaining Information About an Endpoint</span></span>

<span data-ttu-id="aba2b-121">Dans l’infrastructure UPnP, les informations de point de terminaison incluent des informations sur une demande et sa source.</span><span class="sxs-lookup"><span data-stu-id="aba2b-121">In the UPnP framework, endpoint information includes information about a request and its source.</span></span> <span data-ttu-id="aba2b-122">Un appareil peut examiner ces informations afin de prendre une décision sur la demande.</span><span class="sxs-lookup"><span data-stu-id="aba2b-122">A device can examine this information in order to make a decision about the request.</span></span>

<span data-ttu-id="aba2b-123">Les informations de point de terminaison sont éventuellement disponibles pour le service implémenté.</span><span class="sxs-lookup"><span data-stu-id="aba2b-123">Endpoint information is optionally available to the implemented service.</span></span> <span data-ttu-id="aba2b-124">L’hôte de l’appareil a accès aux informations de point de terminaison ; Toutefois, l’hôte d’appareil ne communique pas les informations au service implémenté par défaut.</span><span class="sxs-lookup"><span data-stu-id="aba2b-124">The device host has access to endpoint information; however, the device host does not communicate the information to the implemented service by default.</span></span> <span data-ttu-id="aba2b-125">Vous pouvez autoriser l’hôte d’appareil à partager les informations de point de terminaison avec le service implémenté en modifiant l’interface COM dans le fichier IDL (produit par l’outil Utl2idl).</span><span class="sxs-lookup"><span data-stu-id="aba2b-125">You can enable the device host to share the endpoint information with the implemented service by modifying the COM interface in the IDL file (produced by the Utl2idl tool).</span></span> <span data-ttu-id="aba2b-126">Vous pouvez ajouter un \[ \] paramètre in à chaque méthode qui requiert des informations de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="aba2b-126">You can add an \[in\] parameter to each method that requires endpoint information.</span></span> <span data-ttu-id="aba2b-127">Le \[ paramètre in supplémentaire \] doit être le premier de la liste d’arguments, un pointeur vers une interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) et un nom explicite **punkRemoteEndpointInfo**.</span><span class="sxs-lookup"><span data-stu-id="aba2b-127">The additional \[in\] parameter must be the first one in the list of arguments, a pointer to an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface, and explicitly named **punkRemoteEndpointInfo**.</span></span> <span data-ttu-id="aba2b-128">Les modifications apportées au XML du service ne sont pas requises ou recommandées.</span><span class="sxs-lookup"><span data-stu-id="aba2b-128">Modifications to the Service XML are not required, or recommended.</span></span> <span data-ttu-id="aba2b-129">L’exemple suivant illustre la nouvelle définition de la méthode **PowerOn** lorsqu’elle est modifiée afin de recevoir des informations sur le point de terminaison :</span><span class="sxs-lookup"><span data-stu-id="aba2b-129">The following example shows the new definition of the **PowerOn** method when it is amended so that it receives endpoint information:</span></span>

<span data-ttu-id="aba2b-130">"HRESULT PowerOn ( \[ dans \] IUnknown \* punkRemoteEndpointInfo);"</span><span class="sxs-lookup"><span data-stu-id="aba2b-130">"HRESULT PowerOn(\[in\] IUnknown \*punkRemoteEndpointInfo);"</span></span>

<span data-ttu-id="aba2b-131">Un pointeur vers un objet d’informations de point de terminaison, une interface [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) , est passé par l’hôte de l’appareil à travers ce nouveau paramètre.</span><span class="sxs-lookup"><span data-stu-id="aba2b-131">A pointer to an endpoint information object, an [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) interface, is passed through this new parameter by the device host.</span></span> <span data-ttu-id="aba2b-132">L’interface **IUPnPRemoteEndpointInfo** fournit trois méthodes pour accéder aux informations de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="aba2b-132">The **IUPnPRemoteEndpointInfo** interface provides three methods for accessing the endpoint information.</span></span> <span data-ttu-id="aba2b-133">Vous devez appeler la méthode appropriée pour récupérer les informations de point de terminaison requises par l’implémentation de service.</span><span class="sxs-lookup"><span data-stu-id="aba2b-133">You must call the appropriate method to get the endpoint information that is required by the service implementation.</span></span>

<span data-ttu-id="aba2b-134">En guise d’alternative à la modification manuelle de l’interface COM, vous pouvez utiliser l’outil Utl2idl avec le commutateur **-ci** .</span><span class="sxs-lookup"><span data-stu-id="aba2b-134">As an alternative to manual modification of the COM interface, you can use the Utl2idl tool with the **-ci** switch.</span></span> <span data-ttu-id="aba2b-135">Ce commutateur fait en sorte que l’outil ajoute le paramètre d’informations de point de terminaison à chacune des méthodes dans l’interface COM.</span><span class="sxs-lookup"><span data-stu-id="aba2b-135">This switch causes the tool to add the endpoint information parameter to each of the methods in the COM interface.</span></span> <span data-ttu-id="aba2b-136">L’utilisation du commutateur **-ci** ne facilite pas la modification des méthodes individuelles.</span><span class="sxs-lookup"><span data-stu-id="aba2b-136">Using the **-ci** switch does not facilitate modification of individual methods.</span></span> <span data-ttu-id="aba2b-137">Si aucune information de point de terminaison n’est requise par toutes les méthodes d’une interface, vous devez ajouter le paramètre manuellement pour produire les implémentations les plus efficaces.</span><span class="sxs-lookup"><span data-stu-id="aba2b-137">If endpoint information is not needed by all methods of an interface, you should add the parameter manually in order to produce the most efficient implementations.</span></span>

## <a name="implementing-a-service-object"></a><span data-ttu-id="aba2b-138">Implémentation d’un objet de service</span><span class="sxs-lookup"><span data-stu-id="aba2b-138">Implementing a Service Object</span></span>

<span data-ttu-id="aba2b-139">Vous devez utiliser l’outil Utl2idl pour traduire chaque description de service d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="aba2b-139">You must use the Utl2idl tool to translate each service description of a device.</span></span>

<span data-ttu-id="aba2b-140">Un objet qui fournit les fonctionnalités d’un service est appelé [*objet de service*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="aba2b-140">An object that provides the functionality for a service is referred to as a [*service object*](s-gly.md).</span></span> <span data-ttu-id="aba2b-141">En plus de fournir des fonctionnalités de service, les objets de service gèrent les erreurs à l’aide de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="aba2b-141">In addition to providing service functionality, service objects handle errors by using the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="aba2b-142">Pour plus d’informations, consultez [utilisation de l’API d’hôte d’appareil avec la technologie UPnP](using-the-device-host-api-with-upnp-technology.md).</span><span class="sxs-lookup"><span data-stu-id="aba2b-142">For more information, see [Using the Device Host API with UPnP Technology](using-the-device-host-api-with-upnp-technology.md).</span></span>

<span data-ttu-id="aba2b-143">Pour garantir la compatibilité avec Visual Basic, qui ne prend pas en charge les \[ paramètres de sortie \] , les paramètres **/direction** de **direction** dans la description de service sont convertis en \[ paramètres in, out \] dans IDL.</span><span class="sxs-lookup"><span data-stu-id="aba2b-143">To ensure compatibility with Visual Basic, which does not support \[out\] parameters, the **direction** out **/direction** parameters in the service description are converted to \[in, out\] parameters in IDL.</span></span> <span data-ttu-id="aba2b-144">Le serveur doit les libérer \[ , paramètres out \] .</span><span class="sxs-lookup"><span data-stu-id="aba2b-144">The server must free these \[in, out\] parameters.</span></span>

## <a name="implementing-a-device-control-object"></a><span data-ttu-id="aba2b-145">Implémentation d’un objet de contrôle d’appareil</span><span class="sxs-lookup"><span data-stu-id="aba2b-145">Implementing a Device Control Object</span></span>

<span data-ttu-id="aba2b-146">En plus d’implémenter des objets de service, vous devez implémenter un [*objet de contrôle d’appareil*](d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="aba2b-146">In addition to implementing service objects, you must implement a [*device control object*](d-gly.md).</span></span> <span data-ttu-id="aba2b-147">Un objet de contrôle d’appareil est le point central de gestion et de contrôle des objets de service de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="aba2b-147">A device control object is the central point of management and control for the device's service objects.</span></span> <span data-ttu-id="aba2b-148">Au moment de l’inscription, l’objet de contrôle de l’appareil est passé à l’hôte de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="aba2b-148">At registration time, the device control object is passed to the device host.</span></span> <span data-ttu-id="aba2b-149">Lorsqu’une demande d’abonnement ou de contrôle d’événement arrive pour l’un des services de l’appareil, l’hôte d’appareil appelle dans cet objet de contrôle de périphérique pour obtenir l’objet de service approprié.</span><span class="sxs-lookup"><span data-stu-id="aba2b-149">When an event subscription or control request arrives for one of the device's services, the device host calls into this device control object to obtain the relevant service object.</span></span> <span data-ttu-id="aba2b-150">À ce moment-là, l’objet de contrôle d’appareil crée une instance de l’objet de service ou retourne l’interface d’une instance existante de l’objet de service.</span><span class="sxs-lookup"><span data-stu-id="aba2b-150">At that time, the device control object either creates an instance of the service object or returns the interface of an existing instance of the service object.</span></span>

<span data-ttu-id="aba2b-151">Vous pouvez enregistrer une description de l’appareil sur plusieurs ordinateurs ou plusieurs fois sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="aba2b-151">You can register a device description on multiple computers or multiple times on the same computer.</span></span> <span data-ttu-id="aba2b-152">Étant donné que le nom d’appareil unique (UDN) doit être différent pour chaque instance de l’appareil, l’hôte d’appareil génère un UDN unique pour chaque périphérique et appareil intégré chaque fois que l’appareil est inscrit.</span><span class="sxs-lookup"><span data-stu-id="aba2b-152">Because the Unique Device Name (UDN) must be different for each instance of the device, the device host generates a unique UDN for each device and embedded device each time the device is registered.</span></span> <span data-ttu-id="aba2b-153">Utilisez le UDN spécifié dans le modèle de description de l’appareil pour obtenir les UDN réels générés par l’hôte d’appareil et associés à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="aba2b-153">Use the UDN specified in the device description template to obtain the actual UDN generated by the device host and associated with the device.</span></span> <span data-ttu-id="aba2b-154">Pour annuler l’inscription d’un appareil, vous devez utiliser l’ID fourni par l’infrastructure UPnP lors de l’inscription de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="aba2b-154">To unregister a device, you must use the ID provided by the UPnP framework when the device was registered.</span></span>

<span data-ttu-id="aba2b-155">Les objets de contrôle d’appareil doivent implémenter l’interface [**IUPnPDeviceControl**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) .</span><span class="sxs-lookup"><span data-stu-id="aba2b-155">Device control objects must implement the [**IUPnPDeviceControl**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) interface.</span></span> <span data-ttu-id="aba2b-156">L’hôte d’appareil appelle la méthode [**IUPnPDeviceControl :: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) de l’objet de contrôle d’appareil, en transmettant la description de l’appareil UPnP que l’hôte de périphérique a publié précédemment pour l’appareil et une chaîne d’initialisation spécifiée au moment de l’inscription (voir [inscription d’un appareil hébergé auprès de l’hôte de l’appareil](registering-a-hosted-device-with-the-device-host.md)).</span><span class="sxs-lookup"><span data-stu-id="aba2b-156">The device host invokes the [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) method of the device control object, passing in the UPnP-based device description that the device host previously published for the device and an initialization string that was specified at registration time (see [Registering a Hosted Device with the Device Host](registering-a-hosted-device-with-the-device-host.md)).</span></span> <span data-ttu-id="aba2b-157">À partir de cette description de l’appareil, l’objet contrôle de l’appareil lit les UDNs attribués à chacun des périphériques de l’arborescence des appareils.</span><span class="sxs-lookup"><span data-stu-id="aba2b-157">From this device description, the device control object reads the UDNs assigned to each of the devices in the device tree.</span></span> <span data-ttu-id="aba2b-158">Vous pouvez également utiliser la méthode [**IUPnPRegistrar :: GetUniqueDeviceName**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) pour obtenir ces informations.</span><span class="sxs-lookup"><span data-stu-id="aba2b-158">You can also use the [**IUPnPRegistrar::GetUniqueDeviceName**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) method to obtain this information.</span></span>

<span data-ttu-id="aba2b-159">Lorsque l’hôte d’appareil requiert un pointeur vers un objet de service qui implémente un service particulier, il appelle la méthode [**IUPnPDeviceControl :: GetServiceObject**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) sur l’objet de contrôle d’appareil.</span><span class="sxs-lookup"><span data-stu-id="aba2b-159">When the device host requires a pointer to a service object that implements a particular service, it invokes the [**IUPnPDeviceControl::GetServiceObject**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) method on the device control object.</span></span> <span data-ttu-id="aba2b-160">L’hôte de l’appareil passe le UDN et l’ID de service du service pour lequel il demande un objet de service et l’adresse d’un pointeur [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) sur lequel la méthode est supposée retourner un pointeur vers l’objet de service.</span><span class="sxs-lookup"><span data-stu-id="aba2b-160">The device host passes the UDN and the service ID of the service for which it is requesting a service object and the address of an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer at which the method is expected to return a pointer to the service object.</span></span> <span data-ttu-id="aba2b-161">Le paramètre UDN est nécessaire, car l’objet contrôle de périphérique gère les services pour l’ensemble de l’arborescence des appareils, y compris les périphériques imbriqués.</span><span class="sxs-lookup"><span data-stu-id="aba2b-161">The UDN parameter is necessary because the device control object manages services for the entire device tree, including nested devices.</span></span> <span data-ttu-id="aba2b-162">Si l’hôte de l’appareil demande un appareil imbriqué, **GetServiceObject** utilise le UDN pour l’identifier.</span><span class="sxs-lookup"><span data-stu-id="aba2b-162">If the device host requests a nested device, **GetServiceObject** uses the UDN to identify it.</span></span>

 

 