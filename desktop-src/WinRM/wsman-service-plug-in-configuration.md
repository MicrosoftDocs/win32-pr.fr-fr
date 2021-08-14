---
title: Configuration du plug-in du service WinRM
description: un plug-in de Windows Remote Management (WinRM) doit être inscrit dans le catalogue WinRM pour permettre à l’infrastructure de déterminer de manière dynamique l’ensemble des plug-ins disponibles et les uri de ressource qu’ils prennent en charge.
ms.assetid: d71cd244-3f10-40e3-a756-36cdf41b9cad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b82b24b8631cd6a47a879a6fa0684b9b2ac9c542699396d0f0997afe14cac8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323717"
---
# <a name="winrm-service-plug-in-configuration"></a>Configuration du plug-in du service WinRM

un plug-in de Windows Remote Management (WinRM) doit être inscrit dans le catalogue WinRM pour permettre à l’infrastructure de déterminer de manière dynamique l’ensemble des plug-ins disponibles et les [*uri de ressource*](windows-remote-management-glossary.md) qu’ils prennent en charge. Tous les [*URI de ressource*](windows-remote-management-glossary.md) pour les plug-ins WinRM doivent être conformes au format défini dans la RFC 3986 ( [https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt) ). La configuration s’effectue par le biais du service WinRM principal.

La commande suivante inscrit une configuration de plug-in auprès du service WinRM :

```console
winrm create http://schemas.microsoft.com/wbem/wsman/1/config/plugin?name=MyPlugIn -file:myplugin.xml
```

> [!NOTE]
> Le service WinRM doit être redémarré pour exposer les plug-ins nouvellement inscrits.

La configuration du plug-in est spécifiée au format XML. Voici un exemple.

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



La liste suivante décrit les éléments XML plus en détail et est suivie du schéma de configuration spécifié en tant que XSD.

<dl> <dt>

<span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**PlugInConfiguration** / **OperationsConfiguration**
</dt> <dd>

Spécifie le nom de fichier du plug-in d’opérations. Toutes les variables d’environnement qui sont placées dans cette entrée sont développées dans le contexte des utilisateurs lorsqu’une demande arrive. Chaque utilisateur peut avoir une version différente de la même variable d’environnement, afin que chaque utilisateur puisse se retrouver avec un autre plug-in. Cette entrée ne peut pas être vide et doit pointer vers un plug-in valide.

</dd> <dt>

<span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**PlugInConfiguration** / **Nom**
</dt> <dd>

Spécifie le nom complet à utiliser pour le plug-in. Si une erreur est retournée par le plug-in, ce nom est placé dans le code XML d’erreur renvoyé à l’application cliente. Le nom n'est pas spécifique aux paramètres régionaux.

</dd> <dt>

<span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**PlugInConfiguration** / **Architecture**
</dt> <dd>

Spécifie si le plug-in d’opérations est 32 bits ou 64 bits. Si cet élément n’est pas spécifié, la valeur par défaut est « 32 » sur les systèmes x86 et « 64 » sur les systèmes 64 bits. Pour les systèmes x86, la seule valeur valide est « 32 ». Si la valeur est « 32 » sur un système 64 bits, la redirection WOW64 doit être prise en compte lors de l’entrée des informations de **nom de fichier** . Le système de fichiers sous-jacent utilise la redirection WOW64 pour traduire system32 en SysWOW64. Par exemple, si le **nom de fichier** est « % windir% \\ system32 \\myplugin.dll » et que l' **architecture** est « 32 », le fichier de plug-in réel se trouve dans « % windir% \\ SysWOW64 \\myplugin.dll ».

</dd> <dt>

<span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**PlugInConfiguration** / **XmlRenderingType**
</dt> <dd>

Configure le format dans lequel le code XML est transmis aux plug-ins via l’objet de [**\_ données WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) . Les types suivants sont disponibles :

<dl> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Financière
</dt> <dd>

Les données XML entrantes sont contenues dans une \_ structure de type de données WSMan \_ \_ , qui représente le XML sous la forme d’une mémoire tampon **PCWSTR** .

</dd> <dt>

<span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>Lecteurs
</dt> <dd>

Les données XML entrantes sont contenues dans un \_ type de données WSMan \_ structure de \_ \_ lecteur WS XML \_ , qui représente le XML sous la forme d’un objet **XmlReader** , qui est défini dans le fichier d’en-tête WebServices. h.

</dd> </dl> </dd> <dt>

<span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**PlugInConfiguration** / **InitializationXml**
</dt> <dd>

Ce nœud est facultatif et permet à un plug-in de configurer du code XML supplémentaire qui sera transmis à la méthode [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup). La plupart des plug-ins n’ont pas besoin de ces informations supplémentaires, mais si un plug-in doit être utilisé dans plusieurs scénarios qui nécessitent une sémantique d’exécution différente, ce code XML offre au plug-in la flexibilité nécessaire pour effectuer cette opération.

</dd> <dt>

<span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**PlugInConfiguration** / **Ressources**
</dt> <dd>

Spécifie la liste des [*URI de ressource*](windows-remote-management-glossary.md)que ce plug-in prend en charge. Au moins une entrée **resourceuri** doit être spécifiée ; dans le cas contraire, le code XML sera rejeté.

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**PlugInConfiguration** / **Ressources** / **Ressource**
</dt> <dd>

Représente une configuration d' [*URI de ressource*](windows-remote-management-glossary.md)unique.

> [!Note]  
> L’attribut **SupportsOptions** peut avoir la valeur false. Si **SupportsOptions** a la valeur false, cet attribut n’est pas répertorié lorsque la ressource est énumérée.

 

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**PlugInConfiguration** / **Ressources** / **Ressource** / **Resourceuri**
</dt> <dd>

Spécifie un [*URI de ressource*](windows-remote-management-glossary.md) unique complet ou une chaîne de correspondance partielle basée sur l’attribut **ExactMatch** . Si **ExactMatch** n’est pas présent, la valeur par défaut est **false**, ce qui signifie que le processeur SOAP WinRM effectue une correspondance partielle avec le début de l' *URI de ressource* et, s’il existe une correspondance, la passe au plug-in. L’attribut **SupportsOptions** peut être spécifié si des options sont autorisées pour cet *URI de ressource* . Par défaut, aucune option n’est prise en charge et, si elle est présente dans la demande du client, une erreur est retournée. Si les options sont prises en charge par le plug-in, il est important que le plug-in retourne l’erreur correcte si le plug-in n’est pas compris lorsque l’indicateur **MustUnderstand** a la valeur **true**.

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**PlugInConfiguration** / **Ressources** / **Ressource** / **Fonctionnalité**
</dt> <dd>

Spécifie une fonctionnalité disponible sur cet [*URI de ressource*](windows-remote-management-glossary.md). Il y aura une entrée pour chaque type d’opération qu’elle prend en charge. Les options suivantes sont disponibles :

<dl> <dt>

<span id="Get"></span><span id="get"></span><span id="GET"></span>Télécharger
</dt> <dd>

Les opérations d’extraction sont prises en charge sur l' [*URI de ressource*](windows-remote-management-glossary.md). L’attribut **SupportFragment** est utilisé si l’opération d’extraction prend en charge le concept. L’attribut **SupportFiltering** n’est pas valide et doit avoir la valeur false. Cette fonctionnalité n’est pas valide pour un *URI de ressource* si les opérations de l’interpréteur de commandes sont également prises en charge.

</dd> <dt>

<span id="Put"></span><span id="put"></span><span id="PUT"></span>Posé
</dt> <dd>

Les opérations put sont prises en charge sur l' [*URI de ressource*](windows-remote-management-glossary.md). L’attribut **SupportFragment** est utilisé si l’opération put prend en charge le concept. L’attribut **SupportFiltering** n’est pas valide et doit avoir la valeur **false**. Cette fonctionnalité n’est pas valide pour un *URI de ressource* si les opérations de l’interpréteur de commandes sont également prises en charge.

</dd> <dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>Créés
</dt> <dd>

Les opérations Create sont prises en charge sur l' [*URI de ressource*](windows-remote-management-glossary.md). L’attribut **SupportFragment** est utilisé si l’opération de création prend en charge le concept. L’attribut **SupportFiltering** n’est pas valide et doit avoir la valeur **false**. Cette fonctionnalité n’est pas valide pour un *URI de ressource* si les opérations de l’interpréteur de commandes sont également prises en charge.

</dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>Supprimer
</dt> <dd>

Les opérations de suppression sont prises en charge sur l' [*URI de ressource*](windows-remote-management-glossary.md). L’attribut **SupportFragment** est utilisé si l’opération de suppression prend en charge le concept. L’attribut **SupportFiltering** n’est pas valide et doit avoir la valeur **false**. Cette fonctionnalité n’est pas valide pour un *URI de ressource* si les opérations de l’interpréteur de commandes sont également prises en charge.

</dd> <dt>

<span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>Déclenché
</dt> <dd>

Les opérations d’appel sont prises en charge sur l' [*URI de ressource*](windows-remote-management-glossary.md). L’attribut **SupportFragment** n’est pas pris en charge pour les opérations d’appel et doit avoir la valeur false. L’attribut **SupportFiltering** n’est pas valide et doit avoir la valeur **false**. Cette fonctionnalité n’est pas valide pour un *URI de ressource* si les opérations de l’interpréteur de commandes sont également prises en charge.

</dd> <dt>

<span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>Énumérer
</dt> <dd>

Les opérations d’énumération sont prises en charge sur l' [*URI de ressource*](windows-remote-management-glossary.md). L’attribut **SupportFragment** n’est pas pris en charge pour les opérations d’énumération et doit avoir la valeur **false**. L’attribut **SupportFiltering** est valide, et si le plug-in prend en charge le filtrage, cet attribut doit avoir la valeur **true**. Cette fonctionnalité n’est pas valide pour un *URI de ressource* si les opérations de l’interpréteur de commandes sont également prises en charge.

</dd> <dt>

<span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>Inscrivez
</dt> <dd>

Les opérations d’abonnement sont prises en charge sur l' [*URI de ressource*](windows-remote-management-glossary.md). L’attribut **SupportFragment** n’est pas pris en charge pour les opérations subscribe et doit être défini sur **false**. L’attribut **SupportFiltering** n’est pas valide et doit avoir la valeur **false**. Cette fonctionnalité n’est pas valide pour un *URI de ressource* si les opérations de l’interpréteur de commandes sont également prises en charge.

</dd> <dt>

<span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>Shell
</dt> <dd>

Les opérations de Shell sont prises en charge sur l' [*URI de ressource*](windows-remote-management-glossary.md). L’attribut **SupportFragment** n’est pas pris en charge pour les opérations de Shell et doit avoir la valeur **false**. L’attribut **SupportFiltering** n’est pas valide et doit avoir la valeur **false**. Cette fonctionnalité n’est pas valide pour un *URI de ressource* si une autre fonction d’opération est également prise en charge. Si une fonctionnalité de l’interpréteur de commandes est configurée pour un *URI de ressource*, les opérations obtenir, placer, créer, supprimer, appeler et énumérer sont traitées en interne dans le service WinRM pour gérer les interpréteurs de commandes. Par conséquent, le plug-in ne peut pas traiter les opérations elles-mêmes.

</dd> </dl> </dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**PlugInConfiguration** / **Ressources** / **Ressource** / **Sécurité**
</dt> <dd>

Cet élément définit le descripteur de sécurité (via l’attribut **SDDL** ) qui doit être appliqué pour déterminer l’accès à un [*URI de ressource*](windows-remote-management-glossary.md) particulier (via l’attribut **URI** ). Si **ExactMatch** n’est pas présent, l’élément de **sécurité** prend par défaut la **valeur false**, ce qui signifie que le **SDDL** s’applique à tous les *URI de ressource* qui partagent l' **URI** en tant que préfixe. Si **ExactMatch** a la valeur true, le **SDDL** s’applique uniquement à l' **URI** exact spécifié. S’il existe plusieurs entrées de **sécurité** qui peuvent s’appliquer à un *URI de ressource* particulier, la correspondance de préfixe la plus longue est utilisée pour déterminer le **SDDL** approprié. En raison de la correspondance de préfixe la plus longue, si une entrée d' **URI** de correspondance exacte existe, elle est toujours choisie comme l’élément de sécurité approprié.

</dd> </dl>

Voici le schéma de configuration de plug-in spécifié en tant que XSD.

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

 

 




