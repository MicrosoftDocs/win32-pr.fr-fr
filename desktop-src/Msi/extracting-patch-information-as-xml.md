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
# <a name="extracting-patch-information-as-xml"></a>Extraction d’informations sur les correctifs en tant que XML

Les informations de séquencement et d’applicabilité des correctifs retournées par la fonction [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) ou la méthode [**ExtractPatchXMLData**](installer-extractpatchxmldata.md) sont au format d’un objet BLOB XML qui contient les éléments et les attributs identifiés dans cette rubrique. L’objet BLOB XML peut être fourni à [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) et [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) au lieu du fichier correctif complet.

-   L’élément MsiPatch est l’élément supérieur de l’objet BLOB XML et contient des informations sur le correctif.

    L’attribut SchemaVersion spécifie la version de la définition de schéma. Le schéma est spécifié par MSIPatchApplicability. xsd et la version de schéma actuelle est 1.0.0.0. La valeur de l’attribut PatchGUID est le code correctif GUID pour le package de correctifs obtenu à partir de la propriété [**Résumé du numéro de révision**](revision-number-summary.md) dans le flux d’informations de [synthèse](summary-information-stream.md) du correctif. MinMsiVersion est la version minimale de la Windows Installer requise pour installer le correctif obtenu à partir de la propriété [**Résumé du nombre de mots**](word-count-summary.md) .

-   L’élément TargetProduct est un élément conteneur pour les informations relatives à une application ciblée par un correctif.

    Il peut y avoir plusieurs éléments TargetProduct si le correctif peut être appliqué à plusieurs applications. Les informations contenues dans l’élément TargetProduct sont extraites des transformations incorporées dans le correctif.

-   L’élément TargetProductCode contient la valeur de la propriété [**ProductCode**](productcode.md) de l’application cible avant l’application du correctif logiciel.

    Il peut y avoir plusieurs éléments TargetProductCode si le correctif peut être appliqué à plusieurs applications.

-   L’élément UpdatedProductCode contient le GUID du code du produit de l’application cible après l’application du correctif.

    Cet élément est présent uniquement si le correctif modifie la valeur de la propriété [**ProductCode**](productcode.md) . Un correctif qui modifie le **ProductCode** est désigné sous le terme de [mise à niveau majeure](major-upgrades.md).

-   L’élément TargetVersion contient la propriété [**ProductVersion**](productversion.md) de l’application cible avant que le correctif n’ait été appliqué.
-   L’élément UpdateVersion contient la valeur de la propriété [**ProductVersion**](productversion.md) de l’application cible après l’application du correctif logiciel.

    Cet élément est présent uniquement si le correctif modifie la valeur de la propriété [**ProductVersion**](productversion.md) . L’objet BLOB XML pour un correctif qui implémente une [petite mise à jour](small-updates.md), également appelée QFE, n’inclura pas cet élément. L’objet BLOB XML pour un correctif qui implémente une mise à niveau mineure, également appelée Service Pack, comprendra cet élément.

-   L’élément TargetLanguage contient la valeur de la propriété [**ProductLanguage**](productlanguage.md) de l’application cible avant que le correctif n’ait été appliqué.
-   L’élément UpdatedLanguages contient la valeur de la propriété [**ProductLanguage**](productlanguage.md) une fois que le correctif a été appliqué.
-   L’élément UpgradeCode contient la valeur de la propriété [**UpgradeCode**](upgradecode.md) de l’application cible.
-   L’élément ObsoletedPatch contient les codes de correctif (GUID) des correctifs qui sont spécifiés comme obsolètes par ce correctif.

    La liste des correctifs obsolètes est obtenue à partir du [**Résumé du numéro de révision**](revision-number-summary.md) dans le flux d’informations de [synthèse](summary-information-stream.md) du correctif.

-   L’élément SequenceData contient des informations sur le séquencement des correctifs pour le correctif.

    Il peut y avoir plusieurs éléments SequenceData dans l’objet BLOB XML. Chaque élément SequenceData contient les informations d’une ligne de la [table MsiPatchSequence](msipatchsequence-table.md) du correctif. L’élément SequenceData contient un sous-élément ProductCode, SEQUENCE et Attributes pour les informations contenues dans les champs correspondants de la table MsiPatchSequence. Pour obtenir une description de chaque champ, consultez la section [table MsiPatchSequence](msipatchsequence-table.md) .

## <a name="extracting-applicability-information"></a>Extraction des informations d’applicabilité

L’exemple suivant montre comment extraire les informations d’applicabilité d’un correctif logiciel Windows Installer (fichier. msp) à l’aide de [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa). L’objet BLOB XML extrait est basé sur la définition de schéma dans MSIPatchApplicability. xsd et est retourné à szXMLData.


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



L’exemple suivant montre comment extraire les informations de mise en application d’un correctif Windows Installer (fichier. msp) au format XML. L’objet BLOB XML extrait est basé sur la définition de schéma dans MSIPatchApplicability. xsd et est retourné dans strPatchXML.

``` syntax
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")
strPatchXML = installer.ExtractPatchXMLData("c:\example\patch.msp")
```

## <a name="patch-applicability-schema-definition"></a>Définition du schéma de mise en application des correctifs

Copiez le texte suivant dans le bloc-notes ou dans un autre éditeur de texte pour créer le fichier de définition de schéma pour les informations de mise en application des correctifs dans l’objet BLOB XML. Nommez ce fichier MSIPatchApplicability. XSD.

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

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ExtractPatchXMLData**](installer-extractpatchxmldata.md)
</dt> <dt>

[**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
</dt> <dt>

[**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
</dt> <dt>

[**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> </dl>

 

 



