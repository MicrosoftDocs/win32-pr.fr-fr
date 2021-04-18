---
description: Le schéma de profil d’analyse définit un format XML qui peut être utilisé pour stocker les propriétés des éléments d’acquisition d’images Windows (WIA), tels que les scanneurs et les appareils photo.
ms.assetid: e0848db3-652a-45be-a18b-99b82420c586
title: Analyser le schéma de profil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331c52e933e1e6b771c477bdc8a38f1c5f749448
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519312"
---
# <a name="scan-profile-schema"></a><span data-ttu-id="8c649-103">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="8c649-103">Scan Profile Schema</span></span>

<span data-ttu-id="8c649-104">Le schéma de profil d’analyse définit un format XML qui peut être utilisé pour stocker les propriétés des éléments d’acquisition d’images Windows (WIA), tels que les scanneurs et les appareils photo.</span><span class="sxs-lookup"><span data-stu-id="8c649-104">The Scan Profile Schema defines an XML format that can be used to store the properties of Windows Image Acquisition (WIA) items, such as scanners and cameras.</span></span> <span data-ttu-id="8c649-105">Ces fichiers persistants permettent aux applications de fournir une analyse automatique sans demander aux utilisateurs de mémoriser les paramètres de propriété des éléments.</span><span class="sxs-lookup"><span data-stu-id="8c649-105">These persistent files enable applications to provide automatic scanning without requiring users to remember the property settings of the items.</span></span>

<span data-ttu-id="8c649-106">Tout appareil [**IWiaItem2**](-wia-iwiaitem2.md) peut avoir un profil de numérisation.</span><span class="sxs-lookup"><span data-stu-id="8c649-106">Any [**IWiaItem2**](-wia-iwiaitem2.md) device can have a scan profile.</span></span> <span data-ttu-id="8c649-107">Toutefois, les éléments **IWiaItem2** de type WIA la \_ catégorie \_ \_ fichier fini et la racine de catégorie WIA \_ \_ ne peuvent pas avoir de profils.</span><span class="sxs-lookup"><span data-stu-id="8c649-107">However, **IWiaItem2** items of types WIA\_CATEGORY\_FINISHED\_FILE and WIA\_CATEGORY\_ROOT cannot have profiles.</span></span>

<span data-ttu-id="8c649-108">Les profils d’analyse sont créés et gérés par le biais des interfaces [**IScanProfile**](-wia-iscanprofile.md), [**IScanProfileMgr**](-wia-iscanprofilemgr.md)et [**IScanProfileUI**](-wia-iscanprofileui.md) .</span><span class="sxs-lookup"><span data-stu-id="8c649-108">Scan profiles are created and managed through the [**IScanProfile**](-wia-iscanprofile.md), [**IScanProfileMgr**](-wia-iscanprofilemgr.md), and [**IScanProfileUI**](-wia-iscanprofileui.md) interfaces.</span></span> <span data-ttu-id="8c649-109">Les utilisateurs de votre application peuvent modifier les profils de manière limitée à l’aide de la méthode [**IScanProfileUI :: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="8c649-109">Users of your application can modify profiles in limited ways using the [**IScanProfileUI::ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="8c649-110">Tous les profils d’analyse comportent les éléments suivants : `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` et `<Properties>` .</span><span class="sxs-lookup"><span data-stu-id="8c649-110">All scan profiles have the following elements: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>`, and `<Properties>`.</span></span> <span data-ttu-id="8c649-111">Le profil par défaut d’un appareil possède également un `<Default>` élément.</span><span class="sxs-lookup"><span data-stu-id="8c649-111">The default profile of a device also has a `<Default>` element.</span></span>

<span data-ttu-id="8c649-112">L' `<ProfileGUID>` élément et l' `<DeviceID>` élément ne peuvent pas être modifiés une fois le profil de numérisation créé.</span><span class="sxs-lookup"><span data-stu-id="8c649-112">The `<ProfileGUID>` element and the `<DeviceID>` element cannot be changed after the scan profile is created.</span></span> <span data-ttu-id="8c649-113">Les valeurs de l' `<ProfileName>` élément et de l' `<WiaItem>` élément peuvent être modifiées.</span><span class="sxs-lookup"><span data-stu-id="8c649-113">The values of the `<ProfileName>` element and the `<WiaItem>` element can be modified.</span></span> <span data-ttu-id="8c649-114">L' `<Default>` élément peut être ajouté ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="8c649-114">The `<Default>` element can be added or deleted.</span></span> <span data-ttu-id="8c649-115">Cette opération peut être effectuée par programmation à l’aide des méthodes [**IScanProfile :: SetName**](-wia-iscanprofile-setname.md), [**IScanProfile :: SetItem**](-wia-iscanprofile-setitem.md)et [**IScanProfileMgr :: SetDefault**](-wia-iscanprofilemgr-setdefault.md) .</span><span class="sxs-lookup"><span data-stu-id="8c649-115">This can be done programatically using the [**IScanProfile::SetName**](-wia-iscanprofile-setname.md), [**IScanProfile::SetItem**](-wia-iscanprofile-setitem.md), and [**IScanProfileMgr::SetDefault**](-wia-iscanprofilemgr-setdefault.md) methods.</span></span> <span data-ttu-id="8c649-116">Ces propriétés peuvent également être modifiées par les utilisateurs par le biais de la méthode [**IScanProfileUI :: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="8c649-116">These properties can also be changed by users through the [**IScanProfileUI::ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="8c649-117">L' `<Properties>` élément contient des `<Property>` enfants.</span><span class="sxs-lookup"><span data-stu-id="8c649-117">The `<Properties>` element contains `<Property>` children.</span></span> <span data-ttu-id="8c649-118">Utilisez-les pour ajouter n’importe quelle propriété d’élément ou d’appareil WIA au profil.</span><span class="sxs-lookup"><span data-stu-id="8c649-118">Use these to add any WIA item or device property to the profile.</span></span> <span data-ttu-id="8c649-119">Vous pouvez également développer votre propre image acquisition `<Property>` Children.</span><span class="sxs-lookup"><span data-stu-id="8c649-119">You can also develop your own image acquistion `<Property>` children.</span></span> <span data-ttu-id="8c649-120">Cela rend le schéma de profil d’analyse extensible.</span><span class="sxs-lookup"><span data-stu-id="8c649-120">This makes the Scan Profile Schema extensible.</span></span> <span data-ttu-id="8c649-121">(Pour plus d’informations sur l’extension du schéma, consultez [définition des propriétés personnalisées](-wia-defining-custom-properties.md), [**IScanProfile :: GetProperty**](-wia-iscanprofile-getproperty.md)et [**IScanProfile :: SetProperty**](-wia-iscanprofile-setproperty.md).)</span><span class="sxs-lookup"><span data-stu-id="8c649-121">(For more information about extending the schema, see [Defining Custom Properties](-wia-defining-custom-properties.md), [**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md), and [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).)</span></span>

<span data-ttu-id="8c649-122">Voici le schéma complet du profil de numérisation.</span><span class="sxs-lookup"><span data-stu-id="8c649-122">Here is the complete Scan Profile Schema.</span></span> <span data-ttu-id="8c649-123">Voici un exemple de profil.</span><span class="sxs-lookup"><span data-stu-id="8c649-123">A sample profile follows.</span></span>


```
<?xml version="1.0"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema"
            targetNamespace="https://www.microsoft.com"
            xmlns="https://www.microsoft.com"
            elementFormDefault="qualified">

<xs:element name="ScanProfile">
            <xs:complexType>
            <xs:sequence>
                        <xs:element name="ProfileGUID" type="xs:string"/>
                        <xs:element name="DeviceID" type="xs:string"/>
<xs:element name="ProfileName" type="xs:string"/>
                        <xs:element name="Default" minOccurs="0">
                                    <xs:complexType>
                                    </xs:complexType>
                        </xs:element>
                        <xs:element name="WiaItem" type="xs:string"/>
                        <xs:element name="Properties" type="Properties"/>
            </xs:sequence>
            </xs:complexType>
</xs:element>
 
<xs:complexType name="Properties">
<xs:sequence>
            <xs:element name="Property" maxOccurs="unbounded" minOccurs="0">
            <xs:complexType>
            <xs:simpleContent>
                        <xs:extension base="xs:string">
                                    <xs:attribute name="id" type="xs:integer" use="required"/>
                                    <xs:attribute name="type" type="xs:integer" use="required"/>
                        </xs:extension>
            </xs:simpleContent>
            </xs:complexType>
            </xs:element>
</xs:sequence>
</xs:complexType>
 
</xs:schema>
```



<span data-ttu-id="8c649-124">Cliquez sur **afficher l’exemple** pour afficher un exemple de profil.</span><span class="sxs-lookup"><span data-stu-id="8c649-124">Click **Show Example** to see a sample profile.</span></span>


```
<ScanProfile>
    <ProfileGUID>
        {F862E217-32B0-4396-987A-2191224925CD}
    </ProfileGUID>
    <DeviceID>
        {6BDD1FC6-810F-11D0-BEC7-08002BE2092F}\0001
    </DeviceID>
    <ProfileName>
        Last used settings
    </ProfileName>
    <WiaItem>
        {FB607B1F-43F3-488B-855B-FB703EC342A6}
    </WiaItem>
    <Properties>
        <Property id="4103" type="3">
            3
        </Property>
        <Property id="4106" type="72">
            {B96B3CAB-0728-11D3-9D7B-0000F81EF32E}
        </Property>
        <Property id="6147" type="3">
            300
        </Property>
        <Property id="6154" type="3">
            0
        </Property>
        <Property id="6155" type="3">
            0
        </Property>
    </Properties>
</ScanProfile>
```



## <a name="related-topics"></a><span data-ttu-id="8c649-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8c649-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8c649-126">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="8c649-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8c649-127">**IScanProfile :: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="8c649-127">**IScanProfile::GetProperty**</span></span>](-wia-iscanprofile-getproperty.md)
</dt> <dt>

[<span data-ttu-id="8c649-128">**IScanProfile :: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="8c649-128">**IScanProfile::SetProperty**</span></span>](-wia-iscanprofile-setproperty.md)
</dt> <dt>

<span data-ttu-id="8c649-129">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="8c649-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8c649-130">Constantes de propriété WIA</span><span class="sxs-lookup"><span data-stu-id="8c649-130">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="8c649-131">Définition des propriétés personnalisées</span><span class="sxs-lookup"><span data-stu-id="8c649-131">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 



