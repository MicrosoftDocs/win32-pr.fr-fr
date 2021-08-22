---
description: Lors de l’écriture d’un fournisseur de haute performance qui dérive des classes de Win32 \_ PerfRawData, vous devez suivre des conventions spécifiques afin que WMI puisse fournir des données aux valeurs de propriété.
ms.assetid: 04abb2f9-800f-497a-ac8f-8ef210746273
ms.tgt_platform: multiple
title: Prise en charge de la classe Win32_PerfRawData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70c9899c88849c70265b019c1d73021c61cae4758c41f462349537bd2e806ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050117"
---
# <a name="supporting-the-win32_perfrawdata-class"></a>Prise en charge de la \_ classe Win32 PerfRawData

Lors de l’écriture d’un fournisseur de haute performance qui dérive des classes de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), vous devez suivre des conventions spécifiques afin que WMI puisse fournir des données aux valeurs de propriété.

> [!Note]  
> l’écriture d’un fournisseur de performances élevées WMI pour créer des compteurs de performance n’est pas recommandée sur une version du système d’exploitation Windows. Pour plus d’informations, consultez [création d’un fournisseur d’instances dans un fournisseur de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)et [bibliothèques de performances et WMI](performance-libraries-and-wmi.md).

 

La procédure suivante décrit comment prendre en charge la classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) avec votre fournisseur hautes performances.

**Pour prendre en charge la \_ classe Win32 PerfRawData**

1.  Créez votre classe dans l' \\ espace de noms CIMV2 racine.

    La classe doit être dérivée de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) et le qualificateur **HiPerf** doit avoir la valeur **true**. Vous pouvez également ajouter des classes de données de performance WDM (pilote) à l' \\ espace de noms WMI racine. Pour plus d’informations sur la création de votre propre classe pour WMI, consultez [conception de classes format MOF (MOF)](designing-managed-object-format--mof--classes.md).

2.  Spécifiez le fournisseur en tant que « NT5 \_ GenericPerfProvider \_ v1 » dans le qualificateur du **fournisseur** .
3.  Spécifiez les qualificateurs au niveau de la classe suivants :

    -   **HiPerf**
    -   **Paramètres régionaux**
    -   **PerfDetail**
    -   **Fournisseur**

    Pour plus d’informations, consultez [**qualificateurs de classe pour les classes de compteur de performance**](class-qualifiers-for-performance-counter-classes.md). Ne définissez pas le qualificateur **GenericPerfCtr** , car il est réservé au processus adap qui transfère les données de la bibliothèque de performances dans des classes WMI.

4.  Renseignez les propriétés timestamp et Frequency appropriées utilisées pour calculer des formules de type compteur.

    Ces propriétés sont héritées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) et, si vous écrivez un fournisseur de haute performance, vous devez les remplir pour que la classe s’affiche dans le moniteur système.

5.  Incluez une propriété de clé appelée **Name** dans votre classe (cette propriété n’est pas requise pour les classes singleton).

    Vous ne devez pas utiliser de propriété de clé autre que le **nom** de votre classe.

6.  Créer des propriétés données de type **DWORD** (**UInt32**) ou **QWord** (**UInt64**). Ces propriétés deviennent des compteurs de performance lorsqu’elles sont transférées vers les bibliothèques de performances.
7.  Spécifiez les qualificateurs de niveau de propriété suivants pour toutes les propriétés de votre classe :

    -   **DisplayName**
    -   **CounterType**
    -   **DefaultScale**
    -   **Description**
    -   **PerfDefault**
    -   **PerfDetail**

    Pour plus d’informations, consultez [**qualificateurs de propriété pour les classes de compteur de performance**](property-qualifiers-for-performance-counter-classes.md). En outre, le fichier d’en-tête Winperf. h **contient des valeurs** que vous pouvez spécifier pour **PerfDetail** et.

    WMI utilise les qualificateurs **DisplayName**, **locale** et **Description** pour la localisation. Vous devez ajouter des qualificateurs modifiés à l' \_ espace de noms MS 409 (anglais) afin que le moniteur système puisse afficher correctement les données de votre classe. Cela signifie que vous modifiez la définition de propriété en ajoutant un qualificateur de **Description** avec un texte explicatif et en complétant la valeur **DisplayName** . Vous devez également ajouter des qualificateurs modifiés à tout autre espace de noms de paramètres régionaux pris en charge par votre classe. Si un utilisateur demande des données à partir de paramètres régionaux pour lesquels vous ne fournissez pas de qualificateurs modifiés, WMI prend par défaut les définitions spécifiées dans l' \_ espace de noms MS 409.

8.  Créez une propriété de base pour toute propriété dont le type de compteur attend une valeur de base.

    Cette propriété suit immédiatement la propriété et est nommée * PropertyName ***\_ base**. Par exemple, la propriété moyenne **AvgDiskBytesPerRead** de la [**classe \_ \_ \_ disque logique Win32 PerfRawData Perfdisk**](./retrieving-raw-and-formatted-performance-data.md) requiert une propriété de base nommée **AvgDiskBytesPerRead \_ base** pour compter le nombre d’échantillons. Pour déterminer si le type de compteur que vous souhaitez utiliser requiert une propriété de base, recherchez le type de compteur par nom ou valeur décimale dans les [types de compteurs de performance WMI](wmi-performance-counter-types.md).

9.  Assurez-vous que votre fournisseur répond aux [exigences de performances](supporting-the-win32-perfformatteddata-class.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’un fournisseur d’instances dans un fournisseur de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
