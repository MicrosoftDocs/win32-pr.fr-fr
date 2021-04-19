---
description: Lors de l’écriture d’un fournisseur de haute performance qui dérive des classes de Win32 \_ PerfFormattedData, vous devez suivre des conventions spécifiques afin que WMI puisse calculer les valeurs de propriété.
ms.assetid: 57912f6f-45ca-491c-8a6c-77e2a6937ccc
ms.tgt_platform: multiple
title: Prise en charge de la classe Win32_PerfFormattedData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54911105f5c485d3a80ddb93b96f0af2637c9506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521940"
---
# <a name="supporting-the-win32_perfformatteddata-class"></a>Prise en charge de la \_ classe Win32 PerfFormattedData

Lors de l’écriture d’un fournisseur de haute performance qui dérive des classes de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), vous devez suivre des conventions spécifiques afin que WMI puisse calculer les valeurs de propriété.

> [!Note]  
> L’écriture d’un fournisseur de performances élevées WMI pour créer des compteurs de performance n’est pas recommandée sur une version du système d’exploitation Windows. Pour plus d’informations, consultez [création d’un fournisseur d’instances dans un fournisseur de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)et [bibliothèques de performances et WMI](performance-libraries-and-wmi.md).

 

La procédure suivante décrit comment prendre en charge la \_ classe Win32 PerfFormattedData.

**Pour prendre en charge la \_ classe Win32 PerfFormattedData**

1.  Créez votre classe dans le même espace de noms que la classe brute correspondante. La classe doit être dérivée de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) et le qualificateur **HiPerf** doit avoir la valeur **true**. Pour plus d’informations sur la création de votre propre classe pour WMI, consultez [conception de classes format MOF (MOF)](designing-managed-object-format--mof--classes.md).
2.  Spécifiez « HiPerfCooker \_ v1 » dans le qualificateur du [**fournisseur**](class-qualifiers-for-performance-counter-classes.md) .
3.  Spécifiez les qualificateurs au niveau de la classe suivants en plus des qualificateurs utilisés pour les classes brutes :

    -   [**Cook automatique**](class-qualifiers-for-performance-counter-classes.md)
    -   [**RawClass autocook \_**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Cuisson**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Réduis**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Dynamique**](dynamic-qualifier.md)
    -   [**HiPerf**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Paramètres régionaux**](class-qualifiers-for-performance-counter-classes.md)
    -   [**PerfDefault**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Fournisseur**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Singleton**](standard-wmi-qualifiers.md)

    > [!Note]  
    > Ne définissez pas de valeur pour **GenericPerfCtr**, **PerfIndex** ou **HelpIndex** , car ceux-ci seront définis par le processus adap. Pour plus d’informations, consultez [**qualificateurs de classe pour les classes de compteur de performance**](class-qualifiers-for-performance-counter-classes.md).

     

4.  Incluez une propriété de clé appelée **Name** dans votre classe (cette propriété n’est pas requise pour les classes singleton).

    La valeur de la propriété **Name** doit être la même que la classe brute correspondante. Vous ne devez pas utiliser de propriété de clé autre que le **nom** de votre classe.

5.  Créer des propriétés de données de type **DWORD** (**UInt32**) ou **QWord** (**UInt64**).

    Les propriétés doivent correspondre à une propriété de la classe brute ou à une propriété de la classe que vous créez.

6.  Spécifiez les qualificateurs de niveau de propriété suivants pour toutes les propriétés de votre classe en plus des qualificateurs **PerfIndex** et **PerfDetail** utilisés pour les propriétés de la classe brute :

    -   [**Base**](property-qualifiers-for-performance-counter-classes.md)
    -   [**CookingType**](property-qualifiers-for-performance-counter-classes.md)
    -   [**Compteur**](property-qualifiers-for-performance-counter-classes.md)
    -   [**PerfTimeStamp**](property-qualifiers-for-performance-counter-classes.md)
    -   [**PerfTimeFreq**](property-qualifiers-for-performance-counter-classes.md)
    -   [**SampleWindow**](property-qualifiers-for-performance-counter-classes.md)

    Pour plus d’informations, consultez [**qualificateurs de propriété pour les classes de compteur de performance**](property-qualifiers-for-performance-counter-classes.md). En outre, le fichier d’en-tête Winperf. h **contient des valeurs** que vous pouvez spécifier pour **PerfDetail** et.

7.  Assurez-vous que votre fournisseur répond aux [exigences de performances](#performance-requirements).

## <a name="performance-requirements"></a>Exigences en matière de performances

Lorsque vous écrivez un fournisseur à hautes performances, ses performances doivent remplir les conditions suivantes :

-   L’ouverture du fichier DLL à hautes performances ne peut pas durer plus de 100 millisecondes. Globalement, l’ouverture de chaque fournisseur de performances et de la bibliothèque de performances ne peut pas dépasser 5 secondes.
-   L’actualisation des données ne peut pas durer plus de 10 millisecondes par collecte. Dans le cas d’une opération d’actualisation et de collecte globale, l’ensemble des fournisseurs hautes performances ne peut pas prendre plus de 800 millisecondes.
-   La charge de l’UC globale pour tous les fournisseurs à hautes performances ne peut pas dépasser 6-7% de la surcharge de l’UC de manière interactive ou 5% pour la journalisation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’un fournisseur d’instances dans un fournisseur de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
