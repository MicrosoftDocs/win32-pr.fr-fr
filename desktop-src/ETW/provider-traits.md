---
description: Les caractéristiques du fournisseur sont une méthode qui consiste à attacher plus de données à une inscription de fournisseur individuel.
ms.assetid: 97755D64-BF57-4C0D-8ED4-040FC375C4AF
title: Caractéristiques du fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c67b25857070edb6419be9a2898d2667f3a179d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973570"
---
# <a name="provider-traits"></a>Caractéristiques du fournisseur

Les caractéristiques du fournisseur sont une méthode qui consiste à attacher plus de données à une inscription de fournisseur individuel. Elles peuvent être utilisées pour les fournisseurs TraceLogging ou basés sur un manifeste. Cela comprend actuellement la prise en charge de l’ajout d’un nom de fournisseur et/ou d’un groupe de fournisseurs à l’inscription d’un fournisseur individuel. D’autres types de caractéristiques sont susceptibles d’être ajoutés à l’avenir. Ces informations sont stockées dans le noyau sous la forme d’un objet blob binaire d’un format défini.

Les caractéristiques ne peuvent être définies qu’une seule fois pour une inscription. Toute nouvelle tentative de définition des caractéristiques de cette inscription échouera.

Pour définir des caractéristiques de fournisseur sur un fournisseur basé sur un manifeste, appelez la fonction [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) avec la classe d’informations EventProviderSetTraits. La mémoire tampon EventInformation doit contenir un blob binaire au format suivant :

``` syntax
{
   UINT16 TraitsSize   // Total size of the traits including this field
   CHAR[] ProviderName // Null terminated utf-8 provider name
   TRAIT[] Traits      // Zero or more individual traits
}
```

Les caractéristiques individuelles doivent être au format suivant :

``` syntax
TRAIT {
      UINT16 TraitSize // Size of this individual trait including this field
      UINT8 Type       // ETW_PROVIDER_TRAIT_TYPE
      BYTE[] Data
      }
```

À partir de la caractéristique individuelle, le \_ type de caractéristique du fournisseur ETW \_ \_ est défini comme suit :

``` syntax
typedef enum {
    EtwProviderTraitTypeGroup = 1,
    EtwProviderTraitTypeMax
} ETW_PROVIDER_TRAIT_TYPE;
```

Les fournisseurs TraceLogging définissent automatiquement les caractéristiques du fournisseur lorsque la fonction [**TraceLoggingRegister**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) est appelée. Le nom du fournisseur TraceLogging sera toujours inclus dans ses caractéristiques. Un groupe peut être défini sur un fournisseur TraceLogging à l’aide de la macro [**TraceLoggingOptionGroup**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) dans la définition du fournisseur.

## <a name="custom-traits"></a>Caractéristiques personnalisées

Bien que la plupart des 255 types de caractéristiques possibles ne soient pas encore définis, les types de traits 1-127 sont réservés à la définition par Microsoft. Les autres valeurs de type indexées restantes peuvent être utilisées par les développeurs externes comme ils le voient. Toute personne prenant en compte l’ajout de ses propres caractéristiques personnalisées à son fournisseur doit essayer de conserver sa taille de trait totale sous 256 octets pour les raisons suivantes :

-   Les caractéristiques sont incluses dans chaque événement écrit pour le fournisseur. Les grandes caractéristiques peuvent entraîner des fichiers journaux de très grande taille.
-   Les caractéristiques sont stockées dans le pool de noyaux non paginé pour la durée de vie du fournisseur.

## <a name="provider-groups"></a>Groupes de fournisseurs

Un groupe de fournisseurs est une entité contrôlable définie par GUID, à l’instar d’un fournisseur lui-même. La principale différence réside dans le fait que lorsqu’un GUID de fournisseur est utilisé pour contrôler les inscriptions de son fournisseur uniquement, un groupe contrôlera l’ensemble de ses inscriptions de membres. Par exemple, l’activation d’un groupe de fournisseurs avec un mot clé et un niveau donnés activera tous les enregistrements des membres des groupes avec ce mot clé et ce niveau.

L’appartenance au groupe peut être restreinte par des autorisations. Si l’appelant de [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) ne dispose pas des autorisations nécessaires pour rejoindre le groupe spécifié, l’appartenance est refusée.

Dans certains cas, le contrôleur de session de trace peut souhaiter exclure quelques fournisseurs de l’activation d’un groupe. Pour ce faire, vous pouvez définir une liste d’exclusion. Une liste d’exclusion est une liste de GUID de fournisseur qui ne sera pas activée en fonction des paramètres de groupe pour une seule session de journalisation. Les listes d’interdiction de liste peuvent être modifiées de manière dynamique avec [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) et la classe d’informations TraceSetDisallowList.

Alors que la plupart des actions d’activation peuvent être effectuées pour les groupes de fournisseurs de la même manière que les fournisseurs individuels, il existe certaines exceptions. Voici certaines exceptions :

-   Les groupes de fournisseurs ne peuvent pas être contrôlés par les sessions de suivi privées.
-   Le nom d’événement, l’ID d’événement et les filtres de charge ne sont pas applicables aux groupes de fournisseurs, car ils prennent en charge des informations spécifiques d’un fournisseur individuel.

 

 
