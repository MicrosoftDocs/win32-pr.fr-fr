---
description: Un qualificateur est une chaîne de données qui fournit plus d’informations sur une classe, une instance, une propriété, une méthode ou un paramètre.
ms.assetid: 6984b575-b365-49dd-aeab-a763430f434c
ms.tgt_platform: multiple
title: Ajout d’un qualificateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a6f18f2b79bcd25b2b4ca75811157c9091e6eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542999"
---
# <a name="adding-a-qualifier"></a>Ajout d’un qualificateur

Un qualificateur est une chaîne de données qui fournit plus d’informations sur une classe, une instance, une propriété, une méthode ou un paramètre.

La définition de classe suivante est un exemple de classe dérivée qui a des qualificateurs de classe.

``` syntax
[Dynamic, Provider ("ProviderX")] 
class MyDerivedClass : MyClass
{
    [key] string sKey;
    [Implemented] sint32 ValueMethod();
    [Implemented] sint32 MyMethod ([in, Id(0)] sint32 Param);
};
```

Les qualificateurs peuvent être divisés en qualificateurs standard, qualificateurs CIM et qualificateurs uniques :

-   Qualificateur standard

    Un qualificateur standard est un qualificateur défini par WMI et couramment utilisé dans le code MOF. Par exemple, les qualificateurs [**Dynamic**](dynamic-qualifier.md) et [**Read**](standard-qualifiers.md) sont à la fois des qualificateurs standard. Pour plus d’informations, consultez [qualificateurs WMI](wmi-qualifiers.md).

-   Qualificateur CIM

    Un qualificateur CIM est un qualificateur inclus dans la spécification CIM. Si vous utilisez des qualificateurs CIM dans du code MOF, les qualificateurs standard sont conçus spécifiquement avec WMI à l’esprit. Pour plus d’informations, consultez la [spécification CIM](https://www.dmtf.org/spec/cims.html/)de la DMTF.

-   Qualificateur unique

    Un qualificateur unique est un qualificateur défini spécifiquement pour une nouvelle classe par un fournisseur de classe. Par exemple, le qualificateur [**Units**](standard-qualifiers.md) est un qualificateur non standard, spécifique au fournisseur. Vous pouvez créer vos propres qualificateurs à utiliser avec votre fournisseur. Pour plus d’informations sur la création d’un fournisseur, consultez [développement d’un fournisseur WMI](developing-a-wmi-provider.md).

Quel que soit votre qualificateur, le processus principal que vous effectuez consiste à utiliser le qualificateur dans votre code MOF. Pour plus d’informations, consultez [application d’un qualificateur](applying-a-qualifier.md). Vous pouvez décrire plus en détail un qualificateur avec une version de qualificateur. Une version de qualificateur contient plus d’informations sur la façon dont un fournisseur doit utiliser un qualificateur. Pour plus d’informations, consultez [Description d’un qualificateur avec une version de qualificateur](describing-a-qualifier-with-a-qualifier-flavor.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conception de classes format MOF (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



