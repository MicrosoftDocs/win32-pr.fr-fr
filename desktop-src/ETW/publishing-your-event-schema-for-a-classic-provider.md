---
description: Les fournisseurs classiques doivent utiliser format MOF (MOF) pour publier la disposition de leurs données d’événement. Les consommateurs peuvent ensuite lire la disposition publiée à partir de WMI au moment de l’exécution et l’utiliser pour lire les données d’événement.
ms.assetid: eb3d8422-2352-47cf-9825-cba9916791a9
title: Publication de votre schéma d’événement pour un fournisseur Classic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607e2e9b940df5afd6e8070e9235fe40566ef2b6d2b31b3c14656756835bab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069819"
---
# <a name="publishing-your-event-schema-for-a-classic-provider"></a>Publication de votre schéma d’événement pour un fournisseur Classic

Les fournisseurs [classiques](about-event-tracing.md) doivent utiliser [format MOF](../wmisdk/managed-object-format--mof-.md) (MOF) pour publier la disposition de leurs données d’événement. Les consommateurs peuvent ensuite lire la disposition publiée à partir de WMI au moment de l’exécution et l’utiliser pour lire les données d’événement.

Si vous utilisez MOF pour publier la disposition de vos données d’événement dans WMI, vous créez généralement les trois types de classes MOF suivants dans l' \\ espace de noms WMI racine :

-   [Classe de fournisseur MOF](#provider-mof-classes)
-   [Une ou plusieurs classes MOF d’événements](#event-mof-classes)
-   [Une ou plusieurs classes MOF de type d’événement](#event-type-mof-classes)

## <a name="provider-mof-classes"></a>Classes MOF du fournisseur

Si vous publiez la disposition de vos données d’événement, vous devez créer une classe MOF qui identifie votre fournisseur. Cette classe doit dériver de la classe MOF **EventTrace** et doit être vide (aucune propriété ou méthode). La classe doit également inclure le qualificateur **GUID** qui identifie le fournisseur de manière unique. Il s’agit du même GUID que celui utilisé lors de l’appel de la fonction [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) pour inscrire votre fournisseur.

## <a name="event-mof-classes"></a>Classes MOF d’événements

Une classe d’événement MOF définit une classe d’événements fournie par le fournisseur. Cette classe dérive de la classe Provider MOF et doit être vide (aucune propriété ou méthode). La classe doit également inclure le qualificateur **GUID** qui identifie de façon unique la classe des événements définis par ses classes enfants. Le fournisseur utilise ce même GUID lors de la définition du membre **GUID** de la structure d' [**\_ \_ en-tête de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .

## <a name="event-type-mof-classes"></a>Classes MOF de type d’événement

Une classe MOF de type d’événement définit les données d’événement réelles. Cette classe dérive de sa classe MOF d’événements parent. Lorsque vous nommez la classe MOF du type d’événement, la Convention consiste à utiliser le nom de classe de l’événement MOF au début du type d’événement nom de classe MOF. Par exemple, si le nom de classe de l’événement MOF est HWConfig et que la classe de type d’événement MOF représente les informations de l’UC, vous devez nommer le type d’événement classe MOF, HWConfig \_ CPU.

Utilisez le qualificateur **eventType** sur la classe du type d’événement MOF pour identifier le type d’événement. Si plusieurs types d’événements utilisent les mêmes données d’événement, ils peuvent utiliser la même classe MOF. Le fournisseur utilise la même valeur de type d’événement pour identifier l’événement lors de la définition du membre de **classe. type** de la structure d' [**\_ \_ en-tête de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .

La classe MOF du type d’événement contient des propriétés. L’ordre de ces propriétés définit la disposition des données d’événement. Le tableau suivant identifie les types de données et les qualificateurs que vous pouvez utiliser pour définir les propriétés. Pour plus d’informations sur les qualificateurs de la propriété et de la classe que vous pouvez utiliser, consultez [qualificateurs MOF du suivi d’événements](event-tracing-mof-qualifiers.md).



| Type de données              | Qualificateurs                        | Description                                                                                                                                                                                                                                                                                                              |
|------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **sint8**, **UInt8**   | **Format**                        | Déclare un entier décimal sur 1 octet. Pour déclarer un caractère ANSI, utilisez le qualificateur **format** et définissez sa valeur sur « c ».                                                                                                                                                                                                  |
| **sint16**, **UInt16** | **Format**                        | Déclare un entier décimal sur 2 octets. Pour indiquer que le nombre est un nombre hexadécimal, utilisez le qualificateur de **format** . Par exemple, format ("x").                                                                                                                                                                               |
| **sint32**, **UInt32** | **Format**                        | Déclare un entier décimal sur 4 octets. Pour indiquer que le nombre est un nombre hexadécimal, utilisez le qualificateur de **format** et définissez sa valeur sur « x ».                                                                                                                                                                                |
| **sint64**, **UInt64** | **Format**                        | Déclare un entier décimal sur 8 octets. Pour indiquer que le nombre est un nombre hexadécimal, utilisez le qualificateur de **format** et définissez sa valeur sur « x ».                                                                                                                                                                                |
| **boolean**            |                                   | Déclare une valeur booléenne. Le consommateur d’événements doit interpréter la valeur comme BOOL (entier sur 4 octets).                                                                                                                                                                                                                        |
| **char16**             |                                   | Déclare un caractère élargi. Le consommateur d’événements doit interpréter les tableaux char16 dans les événements de noyau comme des chaînes de caractères larges. (Utilisez la taille du tableau pour copier la chaîne. Certaines chaînes peuvent contenir des caractères NULL de début.)                                                                                                      |
| **object**             | **Extension**                     | Déclare un objet blob binaire. Le qualificateur d' **extension** indique le type de données dans l’objet BLOB.                                                                                                                                                                                                                              |
| **string**             | **Format**, **StringTermination** | Déclare une valeur de chaîne. Pour indiquer que la chaîne est une chaîne de caractères larges, utilisez le qualificateur de **format** et définissez sa valeur sur « w ». La chaîne est considérée comme une chaîne ANSI si vous ne spécifiez pas le qualificateur de **format** . Pour indiquer comment la chaîne est terminée, utilisez le qualificateur **StringTermination** . <br/> |



 

Pour spécifier un tableau, vous pouvez utiliser des crochets, \[ \] . Les crochets peuvent inclure la taille du tableau. Par exemple :

`[WmiDataId(1), read] uint8 MyGuid[16];`

Vous pouvez également utiliser le qualificateur **Max** pour spécifier la taille d’un tableau. Par exemple :

`[WmiDataId(1), Max(16), read] uint8 MyGuid[];`

Si vous incluez la taille du tableau entre crochets, le compilateur MOF génère le qualificateur Max pour vous.

Il est important d’utiliser le qualificateur **Description** pour chaque propriété. La description doit contenir un nom complet que le consommateur peut utiliser lors de l’affichage des valeurs de propriété.

L’exemple suivant montre le contenu d’un fichier MOF qui décrit un fournisseur, un événement et une classe MOF de type événement.

``` syntax
#pragma namespace("\\\\.\\root\\wmi")

[dynamic: ToInstance, Description("Defines my event provider"),
 Guid("{7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}")]
class MyProvider : EventTrace
{
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."): Amended,
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}")]
class MyCategory : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1)]
class MyCategory_MyEvent : MyCategory
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Class identifier"): Amended, read, Extension("Guid")] object ID;
};
```

Notez que les noms de classe de fournisseur, d’événement et de type d’événement MOF doivent être uniques dans l’ensemble de l’espace de noms. Pour éviter les conflits de noms, vous devez utiliser un nom unique et descriptif pour tous les noms de classe. Les propriétés de classe doivent également être descriptives et uniques au sein de sa hiérarchie de classes : une classe enfant qui contient le même nom de propriété qu’une classe parente remplace la propriété de la classe parente.

Après avoir défini vos classes MOF, utilisez le compilateur MOF pour générer votre schéma d’événement et l’ajouter au référentiel CIM. Les consommateurs peuvent alors lire le schéma à partir du référentiel et lire par programmation les données d’événement. Pour obtenir une description complète de la syntaxe MOF et l’utilisation du compilateur MOF (Mofcomp.exe) pour ajouter vos classes MOF au référentiel CIM, consultez [format MOF](../wmisdk/managed-object-format--mof-.md). pour plus d’informations sur l’utilisation de Wbemtest.exe pour accéder au référentiel CIM, consultez [Windows Management Instrumentation](../wmisdk/wmi-start-page.md) (WMI).

## <a name="versioning-mof-class"></a>Classe MOF de contrôle de version

Si vous ajoutez ou modifiez une classe MOF d’un type d’événement, la Convention consiste à effectuer la version de la classe MOF d’événements et de ses classes MOF d’événements enfants. Pour la version de la classe MOF d’événements en cours, ajoutez \_ VN au nom de la classe, où n est un nombre incrémentiel commençant à 0. S’il s’agit de la première révision de la classe, ajoutez \_ v0 au nom de la classe. Vous devez également ajouter le qualificateur **EventVersion** à la classe. Utilisez le même numéro de version que celui utilisé dans le nom de la classe pour la valeur du qualificateur **EventVersion** .

La nouvelle version de la classe MOF d’événements doit utiliser le même nom et le même qualificateur **GUID** que la classe d’origine. La nouvelle classe peut éventuellement ajouter le qualificateur **EventVersion** . La classe MOF d’événements qui ne contient pas le qualificateur **EventVersion** est considérée comme la version la plus récente, ou si toutes les versions de la classe contiennent un qualificateur **EventVersion** , la classe avec le numéro de version le plus élevé est considérée comme la version la plus récente. Le fournisseur utilise le membre **Class. version** de la structure d' [**\_ \_ en-tête de suivi d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) pour identifier la version de l’événement inclus dans la trace.

L’exemple suivant montre comment effectuer la version d’une classe d’événements MOF.

``` syntax
#pragma namespace("\\\\.\\root\\wmi")
#pragma classflags("forceupdate")

[dynamic: ToInstance, Description("Defines my event provider"),
 Guid("{7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}")]
class MyProvider : EventTrace
{
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."),
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}"),
 EventVersion(1)]
class MyCategory : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1),
 EventName("MyEvent")]
class MyCategory_MyEvent : MyCategory
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Identifier"): Amended, read, Extension("Guid")] object ID;
    [WmiDataId(6), Description("Buffer Size"): Amended, read] uint32 Size;
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."): Amended,
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}"),
 EventVersion(0)]
class MyCategory_V0 : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1)]
class MyCategory_V0_MyEvent : MyCategory_V0
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Identifier"): Amended, read, Extension("Guid")] object ID;
};
```

 

 
