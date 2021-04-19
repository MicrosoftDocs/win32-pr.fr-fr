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
# <a name="implementing-device-behavior"></a>Implémentation du comportement de l’appareil

Le comportement d’un appareil est défini par les services qu’il expose. Chaque service a une description de service qui répertorie ses actions et ses variables d’État. Pris ensemble, ces descriptions de service composent l’interface de service, qui définit la façon dont un point de contrôle peut interagir avec un service. Chaque service doit avoir au moins une action.

Pour implémenter un service, un appareil hébergé doit fournir un objet COM (Component Object Model) qui expose l’interface pour le service. Dans la description du service, les interfaces de service sont spécifiées dans le langage de modèles UPnP (UTL); Toutefois, les interfaces d’objets COM sont généralement spécifiées dans le langage IDL (Interface Definition Language). Vous pouvez également spécifier l’interface COM dans une bibliothèque de types ou un fichier d’en-tête. Le kit de développement logiciel (SDK) de la plateforme comprend l’outil Utl2idl, qui traduit une description de service dans UTL en une interface COM dans IDL.

Les exemples suivants illustrent ce processus de conversion. La description du service est fournie par le développeur de l’appareil et est écrite en UTL.

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

L’étape suivante consiste à exécuter l’outil Utl2idl. Il produit le fichier IDL qui contient l’interface COM. Pour plus d’informations sur les fichiers IDL et le mot clé **interface** , consultez [fichier de définition d’interface (IDL)](/windows/desktop/Midl/interface-definition-idl-file) et [**interface**](/windows/desktop/Midl/interface) dans la référence MIDL.

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
> La valeur de retour est le \[ premier \] paramètre de sortie dans la liste d’arguments dans la description de service ; toutefois, elle est répertoriée en tant que dernier paramètre après translation.
> 
> Tous les autres paramètres restent dans le même ordre.

 

Pour fournir les fonctionnalités du service, implémentez cette interface COM.

## <a name="obtaining-information-about-an-endpoint"></a>Obtention d’informations sur un point de terminaison

Dans l’infrastructure UPnP, les informations de point de terminaison incluent des informations sur une demande et sa source. Un appareil peut examiner ces informations afin de prendre une décision sur la demande.

Les informations de point de terminaison sont éventuellement disponibles pour le service implémenté. L’hôte de l’appareil a accès aux informations de point de terminaison ; Toutefois, l’hôte d’appareil ne communique pas les informations au service implémenté par défaut. Vous pouvez autoriser l’hôte d’appareil à partager les informations de point de terminaison avec le service implémenté en modifiant l’interface COM dans le fichier IDL (produit par l’outil Utl2idl). Vous pouvez ajouter un \[ \] paramètre in à chaque méthode qui requiert des informations de point de terminaison. Le \[ paramètre in supplémentaire \] doit être le premier de la liste d’arguments, un pointeur vers une interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) et un nom explicite **punkRemoteEndpointInfo**. Les modifications apportées au XML du service ne sont pas requises ou recommandées. L’exemple suivant illustre la nouvelle définition de la méthode **PowerOn** lorsqu’elle est modifiée afin de recevoir des informations sur le point de terminaison :

"HRESULT PowerOn ( \[ dans \] IUnknown \* punkRemoteEndpointInfo);"

Un pointeur vers un objet d’informations de point de terminaison, une interface [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) , est passé par l’hôte de l’appareil à travers ce nouveau paramètre. L’interface **IUPnPRemoteEndpointInfo** fournit trois méthodes pour accéder aux informations de point de terminaison. Vous devez appeler la méthode appropriée pour récupérer les informations de point de terminaison requises par l’implémentation de service.

En guise d’alternative à la modification manuelle de l’interface COM, vous pouvez utiliser l’outil Utl2idl avec le commutateur **-ci** . Ce commutateur fait en sorte que l’outil ajoute le paramètre d’informations de point de terminaison à chacune des méthodes dans l’interface COM. L’utilisation du commutateur **-ci** ne facilite pas la modification des méthodes individuelles. Si aucune information de point de terminaison n’est requise par toutes les méthodes d’une interface, vous devez ajouter le paramètre manuellement pour produire les implémentations les plus efficaces.

## <a name="implementing-a-service-object"></a>Implémentation d’un objet de service

Vous devez utiliser l’outil Utl2idl pour traduire chaque description de service d’un appareil.

Un objet qui fournit les fonctionnalités d’un service est appelé [*objet de service*](s-gly.md). En plus de fournir des fonctionnalités de service, les objets de service gèrent les erreurs à l’aide de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Pour plus d’informations, consultez [utilisation de l’API d’hôte d’appareil avec la technologie UPnP](using-the-device-host-api-with-upnp-technology.md).

Pour garantir la compatibilité avec Visual Basic, qui ne prend pas en charge les \[ paramètres de sortie \] , les paramètres **/direction** de **direction** dans la description de service sont convertis en \[ paramètres in, out \] dans IDL. Le serveur doit les libérer \[ , paramètres out \] .

## <a name="implementing-a-device-control-object"></a>Implémentation d’un objet de contrôle d’appareil

En plus d’implémenter des objets de service, vous devez implémenter un [*objet de contrôle d’appareil*](d-gly.md). Un objet de contrôle d’appareil est le point central de gestion et de contrôle des objets de service de l’appareil. Au moment de l’inscription, l’objet de contrôle de l’appareil est passé à l’hôte de l’appareil. Lorsqu’une demande d’abonnement ou de contrôle d’événement arrive pour l’un des services de l’appareil, l’hôte d’appareil appelle dans cet objet de contrôle de périphérique pour obtenir l’objet de service approprié. À ce moment-là, l’objet de contrôle d’appareil crée une instance de l’objet de service ou retourne l’interface d’une instance existante de l’objet de service.

Vous pouvez enregistrer une description de l’appareil sur plusieurs ordinateurs ou plusieurs fois sur le même ordinateur. Étant donné que le nom d’appareil unique (UDN) doit être différent pour chaque instance de l’appareil, l’hôte d’appareil génère un UDN unique pour chaque périphérique et appareil intégré chaque fois que l’appareil est inscrit. Utilisez le UDN spécifié dans le modèle de description de l’appareil pour obtenir les UDN réels générés par l’hôte d’appareil et associés à l’appareil. Pour annuler l’inscription d’un appareil, vous devez utiliser l’ID fourni par l’infrastructure UPnP lors de l’inscription de l’appareil.

Les objets de contrôle d’appareil doivent implémenter l’interface [**IUPnPDeviceControl**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol) . L’hôte d’appareil appelle la méthode [**IUPnPDeviceControl :: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) de l’objet de contrôle d’appareil, en transmettant la description de l’appareil UPnP que l’hôte de périphérique a publié précédemment pour l’appareil et une chaîne d’initialisation spécifiée au moment de l’inscription (voir [inscription d’un appareil hébergé auprès de l’hôte de l’appareil](registering-a-hosted-device-with-the-device-host.md)). À partir de cette description de l’appareil, l’objet contrôle de l’appareil lit les UDNs attribués à chacun des périphériques de l’arborescence des appareils. Vous pouvez également utiliser la méthode [**IUPnPRegistrar :: GetUniqueDeviceName**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-getuniquedevicename) pour obtenir ces informations.

Lorsque l’hôte d’appareil requiert un pointeur vers un objet de service qui implémente un service particulier, il appelle la méthode [**IUPnPDeviceControl :: GetServiceObject**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-getserviceobject) sur l’objet de contrôle d’appareil. L’hôte de l’appareil passe le UDN et l’ID de service du service pour lequel il demande un objet de service et l’adresse d’un pointeur [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) sur lequel la méthode est supposée retourner un pointeur vers l’objet de service. Le paramètre UDN est nécessaire, car l’objet contrôle de périphérique gère les services pour l’ensemble de l’arborescence des appareils, y compris les périphériques imbriqués. Si l’hôte de l’appareil demande un appareil imbriqué, **GetServiceObject** utilise le UDN pour l’identifier.

 

 