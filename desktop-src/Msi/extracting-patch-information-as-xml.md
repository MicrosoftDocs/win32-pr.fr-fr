---
description: Les informations de séquencement et d’applicabilité des correctifs retournées par la fonction MsiExtractPatchXMLData ou la méthode ExtractPatchXMLData sont au format d’un objet BLOB XML qui contient les éléments et les attributs identifiés dans cette rubrique.
ms.assetid: ea40ed1d-1ef9-44f3-8ae8-3d854e308a49
title: Extraction d’informations sur les correctifs en tant que XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e1e594d3ff2870ca1aaf87245c537045f95d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114563"
---
# <a name="extracting-patch-information-as-xml"></a><span data-ttu-id="b265d-103">Extraction d’informations sur les correctifs en tant que XML</span><span class="sxs-lookup"><span data-stu-id="b265d-103">Extracting Patch Information as XML</span></span>

<span data-ttu-id="b265d-104">Les informations de séquencement et d’applicabilité des correctifs retournées par la fonction [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) ou la méthode [**ExtractPatchXMLData**](installer-extractpatchxmldata.md) sont au format d’un objet BLOB XML qui contient les éléments et les attributs identifiés dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="b265d-104">The patch sequencing and applicability information that is returned by the [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) function or the [**ExtractPatchXMLData**](installer-extractpatchxmldata.md) method is in the format of an XML blob that contains the elements and attributes that are identified in this topic.</span></span> <span data-ttu-id="b265d-105">L’objet BLOB XML peut être fourni à [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) et [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) au lieu du fichier correctif complet.</span><span class="sxs-lookup"><span data-stu-id="b265d-105">The XML blob can be provided to [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) and [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) instead of the full patch file.</span></span>

-   <span data-ttu-id="b265d-106">L’élément MsiPatch est l’élément supérieur de l’objet BLOB XML et contient des informations sur le correctif.</span><span class="sxs-lookup"><span data-stu-id="b265d-106">The MsiPatch element is the top element of the XML blob, and contains information about the patch.</span></span>

    <span data-ttu-id="b265d-107">L’attribut SchemaVersion spécifie la version de la définition de schéma.</span><span class="sxs-lookup"><span data-stu-id="b265d-107">The SchemaVersion attribute specifies the version of the schema definition.</span></span> <span data-ttu-id="b265d-108">Le schéma est spécifié par MSIPatchApplicability. xsd et la version de schéma actuelle est 1.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="b265d-108">The schema is specified by MSIPatchApplicability.xsd and the current schema version is 1.0.0.0.</span></span> <span data-ttu-id="b265d-109">La valeur de l’attribut PatchGUID est le code correctif GUID pour le package de correctifs obtenu à partir de la propriété [**Résumé du numéro de révision**](revision-number-summary.md) dans le flux d’informations de [synthèse](summary-information-stream.md) du correctif.</span><span class="sxs-lookup"><span data-stu-id="b265d-109">The value of the PatchGUID attribute is the GUID patch code for the patch package obtained from the [**Revision Number Summary**](revision-number-summary.md) Property in the [Summary Information Stream](summary-information-stream.md) of the patch.</span></span> <span data-ttu-id="b265d-110">MinMsiVersion est la version minimale de la Windows Installer requise pour installer le correctif obtenu à partir de la propriété [**Résumé du nombre de mots**](word-count-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="b265d-110">The MinMsiVersion is the minimum version of the Windows Installer required to install the patch obtained from the [**Word Count Summary**](word-count-summary.md) Property.</span></span>

-   <span data-ttu-id="b265d-111">L’élément TargetProduct est un élément conteneur pour les informations relatives à une application ciblée par un correctif.</span><span class="sxs-lookup"><span data-stu-id="b265d-111">The TargetProduct element is a container element for information about an application that a patch targets.</span></span>

    <span data-ttu-id="b265d-112">Il peut y avoir plusieurs éléments TargetProduct si le correctif peut être appliqué à plusieurs applications.</span><span class="sxs-lookup"><span data-stu-id="b265d-112">There can be multiple TargetProduct elements if the patch can be applied to multiple applications.</span></span> <span data-ttu-id="b265d-113">Les informations contenues dans l’élément TargetProduct sont extraites des transformations incorporées dans le correctif.</span><span class="sxs-lookup"><span data-stu-id="b265d-113">The information in the TargetProduct element is extracted from transforms that are embedded within the patch.</span></span>

-   <span data-ttu-id="b265d-114">L’élément TargetProductCode contient la valeur de la propriété [**ProductCode**](productcode.md) de l’application cible avant l’application du correctif logiciel.</span><span class="sxs-lookup"><span data-stu-id="b265d-114">The TargetProductCode element contains the value of the [**ProductCode**](productcode.md) property of the target application before the patch has been applied.</span></span>

    <span data-ttu-id="b265d-115">Il peut y avoir plusieurs éléments TargetProductCode si le correctif peut être appliqué à plusieurs applications.</span><span class="sxs-lookup"><span data-stu-id="b265d-115">There can be multiple TargetProductCode elements if the patch can be applied to multiple applications.</span></span>

-   <span data-ttu-id="b265d-116">L’élément UpdatedProductCode contient le GUID du code du produit de l’application cible après l’application du correctif.</span><span class="sxs-lookup"><span data-stu-id="b265d-116">The UpdatedProductCode element contains the product code GUID of the target application after the patch is applied.</span></span>

    <span data-ttu-id="b265d-117">Cet élément est présent uniquement si le correctif modifie la valeur de la propriété [**ProductCode**](productcode.md) .</span><span class="sxs-lookup"><span data-stu-id="b265d-117">This element is only present if the patch changes the value of the [**ProductCode**](productcode.md) property.</span></span> <span data-ttu-id="b265d-118">Un correctif qui modifie le **ProductCode** est désigné sous le terme de [mise à niveau majeure](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="b265d-118">A patch that changes the **ProductCode** is referred to as a [Major Upgrade](major-upgrades.md).</span></span>

-   <span data-ttu-id="b265d-119">L’élément TargetVersion contient la propriété [**ProductVersion**](productversion.md) de l’application cible avant que le correctif n’ait été appliqué.</span><span class="sxs-lookup"><span data-stu-id="b265d-119">The TargetVersion element contains the [**ProductVersion**](productversion.md) property of the target application before the patch has been applied.</span></span>
-   <span data-ttu-id="b265d-120">L’élément UpdateVersion contient la valeur de la propriété [**ProductVersion**](productversion.md) de l’application cible après l’application du correctif logiciel.</span><span class="sxs-lookup"><span data-stu-id="b265d-120">The UpdateVersion element contains the value of the [**ProductVersion**](productversion.md) property of the target application after the patch is applied.</span></span>

    <span data-ttu-id="b265d-121">Cet élément est présent uniquement si le correctif modifie la valeur de la propriété [**ProductVersion**](productversion.md) .</span><span class="sxs-lookup"><span data-stu-id="b265d-121">This element is only present if the patch changes the value of the [**ProductVersion**](productversion.md) property.</span></span> <span data-ttu-id="b265d-122">L’objet BLOB XML pour un correctif qui implémente une [petite mise à jour](small-updates.md), également appelée QFE, n’inclura pas cet élément.</span><span class="sxs-lookup"><span data-stu-id="b265d-122">The XML blob for a patch that implements a [Small Update](small-updates.md), also referred to as a QFE, will not include this element.</span></span> <span data-ttu-id="b265d-123">L’objet BLOB XML pour un correctif qui implémente une mise à niveau mineure, également appelée Service Pack, comprendra cet élément.</span><span class="sxs-lookup"><span data-stu-id="b265d-123">The XML blob for a patch that implements a minor upgrade, also referred to as a service pack, will include this element.</span></span>

-   <span data-ttu-id="b265d-124">L’élément TargetLanguage contient la valeur de la propriété [**ProductLanguage**](productlanguage.md) de l’application cible avant que le correctif n’ait été appliqué.</span><span class="sxs-lookup"><span data-stu-id="b265d-124">The TargetLanguage element contains the value of the [**ProductLanguage**](productlanguage.md) property of the target application before the patch has been applied.</span></span>
-   <span data-ttu-id="b265d-125">L’élément UpdatedLanguages contient la valeur de la propriété [**ProductLanguage**](productlanguage.md) une fois que le correctif a été appliqué.</span><span class="sxs-lookup"><span data-stu-id="b265d-125">The UpdatedLanguages element contains the value of the [**ProductLanguage**](productlanguage.md) property after the patch has been applied.</span></span>
-   <span data-ttu-id="b265d-126">L’élément UpgradeCode contient la valeur de la propriété [**UpgradeCode**](upgradecode.md) de l’application cible.</span><span class="sxs-lookup"><span data-stu-id="b265d-126">The UpgradeCode element contains the value of the [**UpgradeCode**](upgradecode.md) property of the target application.</span></span>
-   <span data-ttu-id="b265d-127">L’élément ObsoletedPatch contient les codes de correctif (GUID) des correctifs qui sont spécifiés comme obsolètes par ce correctif.</span><span class="sxs-lookup"><span data-stu-id="b265d-127">The ObsoletedPatch element contains the patch codes (GUIDs) of the patches that are specified as obsolete by this patch.</span></span>

    <span data-ttu-id="b265d-128">La liste des correctifs obsolètes est obtenue à partir du [**Résumé du numéro de révision**](revision-number-summary.md) dans le flux d’informations de [synthèse](summary-information-stream.md) du correctif.</span><span class="sxs-lookup"><span data-stu-id="b265d-128">The list of obsolete patches is obtained from [**Revision Number Summary**](revision-number-summary.md) in the [Summary Information Stream](summary-information-stream.md) of the patch.</span></span>

-   <span data-ttu-id="b265d-129">L’élément SequenceData contient des informations sur le séquencement des correctifs pour le correctif.</span><span class="sxs-lookup"><span data-stu-id="b265d-129">The SequenceData element contains patch sequencing information for the patch.</span></span>

    <span data-ttu-id="b265d-130">Il peut y avoir plusieurs éléments SequenceData dans l’objet BLOB XML.</span><span class="sxs-lookup"><span data-stu-id="b265d-130">There can be multiple SequenceData elements in the XML blob.</span></span> <span data-ttu-id="b265d-131">Chaque élément SequenceData contient les informations d’une ligne de la [table MsiPatchSequence](msipatchsequence-table.md) du correctif.</span><span class="sxs-lookup"><span data-stu-id="b265d-131">Each SequenceData element contains the information in one row of the [MsiPatchSequence table](msipatchsequence-table.md) of the patch.</span></span> <span data-ttu-id="b265d-132">L’élément SequenceData contient un sous-élément ProductCode, SEQUENCE et Attributes pour les informations contenues dans les champs correspondants de la table MsiPatchSequence.</span><span class="sxs-lookup"><span data-stu-id="b265d-132">The SequenceData element contains a ProductCode, Sequence, and Attributes subelement for the information in the corresponding fields in the MsiPatchSequence table.</span></span> <span data-ttu-id="b265d-133">Pour obtenir une description de chaque champ, consultez la section [table MsiPatchSequence](msipatchsequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="b265d-133">See the [MsiPatchSequence table](msipatchsequence-table.md) section for a description of each field.</span></span>

## <a name="extracting-applicability-information"></a><span data-ttu-id="b265d-134">Extraction des informations d’applicabilité</span><span class="sxs-lookup"><span data-stu-id="b265d-134">Extracting Applicability Information</span></span>

<span data-ttu-id="b265d-135">L’exemple suivant montre comment extraire les informations d’applicabilité d’un correctif logiciel Windows Installer (fichier. msp) à l’aide de [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span><span class="sxs-lookup"><span data-stu-id="b265d-135">The following example shows you how to extract the applicability information for a Windows Installer Patch (.msp file) using [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span></span> <span data-ttu-id="b265d-136">L’objet BLOB XML extrait est basé sur la définition de schéma dans MSIPatchApplicability. xsd et est retourné à szXMLData.</span><span class="sxs-lookup"><span data-stu-id="b265d-136">The extracted XML blob is based on the schema definition in MSIPatchApplicability.xsd and returned to szXMLData.</span></span>


```C++
#include <windows.h>
#include <msi.h>

#pragma comment( lib, "msi.lib" )

void main()
{
     TCHAR szPatchPath[] = TEXT("c:\\scratch\\RTM-RTMQFE.msp");
    TCHAR* szXMLData = NULL;
    DWORD cchXMLData = 0;

    UINT uiStatus = ERROR_SUCCESS;

    // Determine size of XML blob buffer.
    if (ERROR_SUCCESS == (uiStatus = MsiExtractPatchXMLData(szPatchPath, 
         /*dwReserved: must be 0*/ 0, szXMLData, &cchXMLData)))
    {
        // cchXMLData now includes size of szXMLData in characters not including terminating NULL
        ++cchXMLData;

        szXMLData = new TCHAR[cchXMLData];
        if (ERROR_SUCCESS == (uiStatus = MsiExtractPatchXMLData(szPatchPath, 
            /*dwReserved: must be 0*/ 0, szXMLData, &cchXMLData)))
        {
            //
            // szXMLData now contains the XML patch applicability blob. This could be
            // provided to MsiDetermineApplicablePatches or MsiDeterminePatchSequence in the
            // proper format to evaluate patch applicability.
            //

        }

        delete [] szXMLData;
        szXMLData = NULL;
    }
}
```



<span data-ttu-id="b265d-137">L’exemple suivant montre comment extraire les informations de mise en application d’un correctif Windows Installer (fichier. msp) au format XML.</span><span class="sxs-lookup"><span data-stu-id="b265d-137">The following example shows you how to extract the applicability information for a Windows Installer Patch (.msp file) in XML form.</span></span> <span data-ttu-id="b265d-138">L’objet BLOB XML extrait est basé sur la définition de schéma dans MSIPatchApplicability. xsd et est retourné dans strPatchXML.</span><span class="sxs-lookup"><span data-stu-id="b265d-138">The extracted XML blob is based on the schema definition in MSIPatchApplicability.xsd and returned in strPatchXML.</span></span>

``` syntax
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")
strPatchXML = installer.ExtractPatchXMLData("c:\example\patch.msp")
```

## <a name="patch-applicability-schema-definition"></a><span data-ttu-id="b265d-139">Définition du schéma de mise en application des correctifs</span><span class="sxs-lookup"><span data-stu-id="b265d-139">Patch Applicability Schema Definition</span></span>

<span data-ttu-id="b265d-140">Copiez le texte suivant dans le bloc-notes ou dans un autre éditeur de texte pour créer le fichier de définition de schéma pour les informations de mise en application des correctifs dans l’objet BLOB XML.</span><span class="sxs-lookup"><span data-stu-id="b265d-140">Copy the following text into Notepad or another text editor to create the schema definition file for the patch applicability information in the XML blob.</span></span> <span data-ttu-id="b265d-141">Nommez ce fichier MSIPatchApplicability. XSD.</span><span class="sxs-lookup"><span data-stu-id="b265d-141">Name this file MSIPatchApplicability.XSD.</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema id="Applicability" 
    targetNamespace="https://www.microsoft.com/msi/patch_applicability.xsd" 
    elementFormDefault="qualified" 
    xmlns="https://www.microsoft.com/msi/patch_applicability.xsd" 
    xmlns:mstns="https://www.microsoft.com/msi/patch_applicability.xsd" 
    xmlns:xs="https://www.w3.org/2001/XMLSchema">
    
    <xs:element name="MsiPatch">
        <xs:complexType>
            <xs:sequence>
                <xs:element name="TargetProduct" minOccurs="1" maxOccurs="unbounded">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element name="TargetProductCode" type="ValidateGUID" />
                            <xs:element name="UpdatedProductCode" type="GUID" minOccurs="0" maxOccurs="1" />
                            <xs:element name="TargetVersion" type="ValidateVersion" />
                            <xs:element name="UpdatedVersion" type="Version" minOccurs="0" maxOccurs="1" />
                            <xs:element name="TargetLanguage" type="ValidateLanguage" />
                            <xs:element name="UpdatedLanguages" type="intList" minOccurs="0" maxOccurs="1" />
                            <xs:element name="UpgradeCode" type="ValidateGUID" />
                            <xs:element name="UpdatedUpgradeCode" type="GUID" minOccurs="0" maxOccurs="1" />
                        </xs:sequence>
                        <xs:attribute name="MinMsiVersion" type="xs:int" />
                    </xs:complexType>
                </xs:element>
                <xs:element name="TargetProductCode" type="GUID" minOccurs="1" maxOccurs="unbounded" />
                <xs:element name="ObsoletedPatch" minOccurs="0" maxOccurs="unbounded" type="GUID" />
                <xs:element name="SequenceData" minOccurs="0" maxOccurs="unbounded">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element name="PatchFamily" type="Identifier" />
                            <xs:element name="ProductCode" type="GUID" minOccurs="0" maxOccurs="1" />
                            <xs:element name="Sequence" type="Version" />
                            <xs:element name="Attributes" type="xs:int" minOccurs="0" maxOccurs="1" />
                        </xs:sequence>
                    </xs:complexType>
                </xs:element>
            </xs:sequence>
            <xs:attribute name="SchemaVersion" type="Version" />
            <xs:attribute name="PatchGUID" type="GUID" />
            <xs:attribute name="MinMsiVersion" type="xs:int" />
            <xs:attribute name="TargetsRTM" type="xs:boolean" use="optional" />
        </xs:complexType>
    </xs:element>
    <xs:simpleType name="GUID">
        <xs:restriction base="xs:string">
            <xs:pattern value="\{[0-9A-Fa-f]{8}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{12}\}" />
        </xs:restriction>
    </xs:simpleType>
    <xs:simpleType name="Version">
        <xs:restriction base="xs:string">
            <xs:pattern value="[0-9]{1,5}(\.[0-9]{1,5}){0,3}" />
        </xs:restriction>
    </xs:simpleType>
    <xs:complexType name="ValidateGUID">
        <xs:simpleContent>
            <xs:extension base="GUID">
                <xs:attribute name="Validate" type="xs:boolean" />
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>
    <xs:complexType name="ValidateVersion">
        <xs:simpleContent>
            <xs:extension base="Version">
                <xs:attribute name="ComparisonType">
                    <xs:simpleType>
                        <xs:restriction base="xs:string">
                            <xs:enumeration value="LessThan" />
                            <xs:enumeration value="LessThanOrEqual" />
                            <xs:enumeration value="Equal" />
                            <xs:enumeration value="GreaterThanOrEqual" />
                            <xs:enumeration value="GreaterThan" />
                            <xs:enumeration value="None" />
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
                <xs:attribute name="ComparisonFilter">
                    <xs:simpleType>
                        <xs:restriction base="xs:string">
                            <xs:enumeration value="Major" />
                            <xs:enumeration value="MajorMinor" />
                            <xs:enumeration value="MajorMinorUpdate" />
                            <xs:enumeration value="None" />
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
                <xs:attribute name="Validate" type="xs:boolean" />
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>
    <xs:complexType name="ValidateLanguage">
        <xs:simpleContent>
            <xs:extension base="xs:int">
                <xs:attribute name="Validate" type="xs:boolean" />
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>
    <xs:simpleType name="intList">
        <xs:list itemType="xs:int" />
    </xs:simpleType>
    <xs:simpleType name="Identifier">
        <xs:restriction base="xs:string">
            <xs:pattern value="[_a-zA-Z][_a-zA-Z0-9\.]*" />
        </xs:restriction>
    </xs:simpleType>
</xs:schema>
```

## <a name="related-topics"></a><span data-ttu-id="b265d-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b265d-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b265d-143">**ExtractPatchXMLData**</span><span class="sxs-lookup"><span data-stu-id="b265d-143">**ExtractPatchXMLData**</span></span>](installer-extractpatchxmldata.md)
</dt> <dt>

[<span data-ttu-id="b265d-144">**MsiDeterminePatchSequence**</span><span class="sxs-lookup"><span data-stu-id="b265d-144">**MsiDeterminePatchSequence**</span></span>](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
</dt> <dt>

[<span data-ttu-id="b265d-145">**MsiDetermineApplicablePatches**</span><span class="sxs-lookup"><span data-stu-id="b265d-145">**MsiDetermineApplicablePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
</dt> <dt>

[<span data-ttu-id="b265d-146">**MsiExtractPatchXMLData**</span><span class="sxs-lookup"><span data-stu-id="b265d-146">**MsiExtractPatchXMLData**</span></span>](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> </dl>

 

 



