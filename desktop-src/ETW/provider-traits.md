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
# <a name="provider-traits"></a><span data-ttu-id="bcd8d-103">Caractéristiques du fournisseur</span><span class="sxs-lookup"><span data-stu-id="bcd8d-103">Provider Traits</span></span>

<span data-ttu-id="bcd8d-104">Les caractéristiques du fournisseur sont une méthode qui consiste à attacher plus de données à une inscription de fournisseur individuel.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-104">Provider Traits are a method of attaching more data to an individual provider registration.</span></span> <span data-ttu-id="bcd8d-105">Elles peuvent être utilisées pour les fournisseurs TraceLogging ou basés sur un manifeste.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-105">They can be used for manifest-based or TraceLogging providers.</span></span> <span data-ttu-id="bcd8d-106">Cela comprend actuellement la prise en charge de l’ajout d’un nom de fournisseur et/ou d’un groupe de fournisseurs à l’inscription d’un fournisseur individuel.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-106">This currently includes support for adding a Provider Name and/or Provider Group to an individual provider registration.</span></span> <span data-ttu-id="bcd8d-107">D’autres types de caractéristiques sont susceptibles d’être ajoutés à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-107">More trait types are likely to be added in the future.</span></span> <span data-ttu-id="bcd8d-108">Ces informations sont stockées dans le noyau sous la forme d’un objet blob binaire d’un format défini.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-108">This information is stored in the kernel as a binary blob of a set format.</span></span>

<span data-ttu-id="bcd8d-109">Les caractéristiques ne peuvent être définies qu’une seule fois pour une inscription.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-109">Traits can only be set once for a registration.</span></span> <span data-ttu-id="bcd8d-110">Toute nouvelle tentative de définition des caractéristiques de cette inscription échouera.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-110">Any further attempts to set the traits on that registration will fail.</span></span>

<span data-ttu-id="bcd8d-111">Pour définir des caractéristiques de fournisseur sur un fournisseur basé sur un manifeste, appelez la fonction [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) avec la classe d’informations EventProviderSetTraits.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-111">To set Provider Traits on a manifest-based provider, call the [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) function with the EventProviderSetTraits information class.</span></span> <span data-ttu-id="bcd8d-112">La mémoire tampon EventInformation doit contenir un blob binaire au format suivant :</span><span class="sxs-lookup"><span data-stu-id="bcd8d-112">The EventInformation buffer should contain a binary blob of the following format:</span></span>

``` syntax
{
   UINT16 TraitsSize   // Total size of the traits including this field
   CHAR[] ProviderName // Null terminated utf-8 provider name
   TRAIT[] Traits      // Zero or more individual traits
}
```

<span data-ttu-id="bcd8d-113">Les caractéristiques individuelles doivent être au format suivant :</span><span class="sxs-lookup"><span data-stu-id="bcd8d-113">Individual traits should be in the following format:</span></span>

``` syntax
TRAIT {
      UINT16 TraitSize // Size of this individual trait including this field
      UINT8 Type       // ETW_PROVIDER_TRAIT_TYPE
      BYTE[] Data
      }
```

<span data-ttu-id="bcd8d-114">À partir de la caractéristique individuelle, le \_ type de caractéristique du fournisseur ETW \_ \_ est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="bcd8d-114">From the individual trait, ETW\_PROVIDER\_TRAIT\_TYPE is defined as:</span></span>

``` syntax
typedef enum {
    EtwProviderTraitTypeGroup = 1,
    EtwProviderTraitTypeMax
} ETW_PROVIDER_TRAIT_TYPE;
```

<span data-ttu-id="bcd8d-115">Les fournisseurs TraceLogging définissent automatiquement les caractéristiques du fournisseur lorsque la fonction [**TraceLoggingRegister**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) est appelée.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-115">TraceLogging providers automatically set the Provider Traits when the [**TraceLoggingRegister**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) function is called.</span></span> <span data-ttu-id="bcd8d-116">Le nom du fournisseur TraceLogging sera toujours inclus dans ses caractéristiques.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-116">The TraceLogging provider's name will always be included in its traits.</span></span> <span data-ttu-id="bcd8d-117">Un groupe peut être défini sur un fournisseur TraceLogging à l’aide de la macro [**TraceLoggingOptionGroup**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) dans la définition du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-117">A group can be set on a TraceLogging provider using the [**TraceLoggingOptionGroup**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) macro in the provider definition.</span></span>

## <a name="custom-traits"></a><span data-ttu-id="bcd8d-118">Caractéristiques personnalisées</span><span class="sxs-lookup"><span data-stu-id="bcd8d-118">Custom Traits</span></span>

<span data-ttu-id="bcd8d-119">Bien que la plupart des 255 types de caractéristiques possibles ne soient pas encore définis, les types de traits 1-127 sont réservés à la définition par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-119">Although most of the 255 possible trait types are not yet defined, trait types 1-127 are reserved for definition by Microsoft.</span></span> <span data-ttu-id="bcd8d-120">Les autres valeurs de type indexées restantes peuvent être utilisées par les développeurs externes comme ils le voient.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-120">The remaining higher indexed type values can be used by external developers as they see fit.</span></span> <span data-ttu-id="bcd8d-121">Toute personne prenant en compte l’ajout de ses propres caractéristiques personnalisées à son fournisseur doit essayer de conserver sa taille de trait totale sous 256 octets pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="bcd8d-121">Anyone considering adding their own custom traits to their provider should try to keep their total trait size under 256 bytes for the following reasons:</span></span>

-   <span data-ttu-id="bcd8d-122">Les caractéristiques sont incluses dans chaque événement écrit pour le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-122">The traits are included in every event written for the provider.</span></span> <span data-ttu-id="bcd8d-123">Les grandes caractéristiques peuvent entraîner des fichiers journaux de très grande taille.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-123">Large traits could lead to very large log files.</span></span>
-   <span data-ttu-id="bcd8d-124">Les caractéristiques sont stockées dans le pool de noyaux non paginé pour la durée de vie du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-124">The traits are stored in nonpaged kernel pool for the lifetime of the provider.</span></span>

## <a name="provider-groups"></a><span data-ttu-id="bcd8d-125">Groupes de fournisseurs</span><span class="sxs-lookup"><span data-stu-id="bcd8d-125">Provider Groups</span></span>

<span data-ttu-id="bcd8d-126">Un groupe de fournisseurs est une entité contrôlable définie par GUID, à l’instar d’un fournisseur lui-même.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-126">A provider group is a GUID-defined controllable entity much like a provider itself.</span></span> <span data-ttu-id="bcd8d-127">La principale différence réside dans le fait que lorsqu’un GUID de fournisseur est utilisé pour contrôler les inscriptions de son fournisseur uniquement, un groupe contrôlera l’ensemble de ses inscriptions de membres.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-127">The key difference is that while a provider GUID is used to control registrations of just its provider, a group will control all of its member registrations.</span></span> <span data-ttu-id="bcd8d-128">Par exemple, l’activation d’un groupe de fournisseurs avec un mot clé et un niveau donnés activera tous les enregistrements des membres des groupes avec ce mot clé et ce niveau.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-128">For example, enabling a provider group with a given keyword and level will enable all of the groups member registrations with that keyword and level.</span></span>

<span data-ttu-id="bcd8d-129">L’appartenance au groupe peut être restreinte par des autorisations.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-129">Group membership may be restricted by permissions.</span></span> <span data-ttu-id="bcd8d-130">Si l’appelant de [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) ne dispose pas des autorisations nécessaires pour rejoindre le groupe spécifié, l’appartenance est refusée.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-130">If the caller of [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) doesn't have permissions to join the specified group, then membership will be denied.</span></span>

<span data-ttu-id="bcd8d-131">Dans certains cas, le contrôleur de session de trace peut souhaiter exclure quelques fournisseurs de l’activation d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-131">In some cases the trace session controller may want to exclude a few providers from its enable of a group.</span></span> <span data-ttu-id="bcd8d-132">Pour ce faire, vous pouvez définir une liste d’exclusion.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-132">This can be done by setting a disallow list.</span></span> <span data-ttu-id="bcd8d-133">Une liste d’exclusion est une liste de GUID de fournisseur qui ne sera pas activée en fonction des paramètres de groupe pour une seule session de journalisation.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-133">A disallow list is a list of provider GUIDs that will not be enabled based on the group settings for a single logging session.</span></span> <span data-ttu-id="bcd8d-134">Les listes d’interdiction de liste peuvent être modifiées de manière dynamique avec [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) et la classe d’informations TraceSetDisallowList.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-134">Disallow lists can be changed dynamically with [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) and the TraceSetDisallowList information class.</span></span>

<span data-ttu-id="bcd8d-135">Alors que la plupart des actions d’activation peuvent être effectuées pour les groupes de fournisseurs de la même manière que les fournisseurs individuels, il existe certaines exceptions.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-135">While most enable actions can be done for Provider Groups in a similar manner to individual providers, there are some exceptions.</span></span> <span data-ttu-id="bcd8d-136">Voici certaines exceptions :</span><span class="sxs-lookup"><span data-stu-id="bcd8d-136">Exceptions include:</span></span>

-   <span data-ttu-id="bcd8d-137">Les groupes de fournisseurs ne peuvent pas être contrôlés par les sessions de suivi privées.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-137">Provider Groups cannot be controlled by private trace sessions.</span></span>
-   <span data-ttu-id="bcd8d-138">Le nom d’événement, l’ID d’événement et les filtres de charge ne sont pas applicables aux groupes de fournisseurs, car ils prennent en charge des informations spécifiques d’un fournisseur individuel.</span><span class="sxs-lookup"><span data-stu-id="bcd8d-138">Event Name, Event ID, and Payload filters are not applicable to Provider Groups as they assume specific information of an individual provider.</span></span>

 

 
