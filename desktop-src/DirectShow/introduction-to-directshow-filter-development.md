---
description: présentation du développement de filtres DirectShow
ms.assetid: d5162ea4-ef37-4993-a82c-782f03b08c64
title: présentation du développement de filtres DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2769cfe3bd4f046c117c0567104094bcad0eed730c388b551593dde6b41df25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083689"
---
# <a name="introduction-to-directshow-filter-development"></a>présentation du développement de filtres DirectShow

cette section fournit un bref aperçu des tâches impliquées dans le développement d’un filtre de DirectShow personnalisé. Il fournit également des liens vers des rubriques qui traitent de ces tâches plus en détail. avant de lire cette section, lisez les rubriques dans [à propos de DirectShow](about-directshow.md), qui décrivent l’architecture globale des DirectShow.

**DirectShow Bibliothèque de classes de base**

le kit de développement logiciel (SDK) DirectShow comprend un ensemble de classes C++ pour l’écriture de filtres. Bien qu’elles ne soient pas requises, ces classes constituent la méthode recommandée pour écrire un nouveau filtre. pour utiliser les classes de base, compilez-les dans une bibliothèque statique et liez le fichier. lib à votre projet, comme décrit dans [génération de filtres de DirectShow](building-directshow-filters.md).

La bibliothèque de classes de base définit une classe racine pour les filtres, la classe [**CBaseFilter**](cbasefilter.md) . Plusieurs autres classes dérivent de **CBaseFilter** et sont spécialisées pour des genres particuliers de filtres. Par exemple, la classe [**CTransformFilter**](ctransformfilter.md) est conçue pour les filtres de transformation. Pour créer un nouveau filtre, implémentez une classe qui hérite de l’une des classes de filtre. Par exemple, votre déclaration de classe peut être la suivante :


```C++
class CMyFilter : public CTransformFilter
{
private:
    /* Declare variables and methods that are specific to your filter.
public:
    /* Override various methods in CTransformFilter */
};
```



pour plus d’informations sur les classes de base de DirectShow, consultez les rubriques suivantes :

-   [DirectShow Classes de base](directshow-base-classes.md)
-   [génération de filtres de DirectShow](building-directshow-filters.md)

**Création de codes confidentiels**

Un filtre doit créer un ou plusieurs codes confidentiels. Le nombre de codes confidentiels peut être corrigé au moment de la conception, ou le filtre peut créer des codes confidentiels en fonction des besoins. Les codes confidentiels dérivent généralement de la classe [**CBasePin**](cbasepin.md) , ou d’une classe qui hérite de **CBasePin**, comme [**CBaseInputPin**](cbaseinputpin.md). Les codes confidentiels du filtre doivent être déclarés en tant que variables de membre dans la classe de filtre. Certaines des classes de filtre définissent déjà les codes confidentiels, mais si votre filtre hérite directement de **CBaseFilter**, vous devez déclarer les codes confidentiels dans votre classe dérivée.

**Négociation des connexions de pin**

lorsque le gestionnaire de Graph de filtre tente de connecter deux filtres, les broches doivent s’entendre sur différentes choses. Si ce n’est pas le cas, la tentative de connexion échoue. En règle générale, les codes confidentiels négocient les éléments suivants :

-   Transport. Le transport est le mécanisme utilisé par les filtres pour déplacer des échantillons de média à partir de la broche de sortie vers la broche d’entrée. Par exemple, ils peuvent utiliser l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) (« push Model ») ou l’interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) (« pull Model »).
-   Type de média. Presque tous les codes confidentiels utilisent des types de médias pour décrire le format des données qu’ils fournissent.
-   Allocateur. L’Allocator est l’objet qui crée les mémoires tampons qui contiennent les données. Les pin doivent s’accorder sur le code confidentiel qui fournira l’allocateur. Ils doivent également accepter la taille des mémoires tampons, le nombre de mémoires tampons à créer et d’autres propriétés de mémoire tampon.

Les classes de base implémentent une infrastructure pour ces négociations. Vous devez compléter les détails en remplaçant différentes méthodes dans la classe de base. L’ensemble de méthodes que vous devez substituer dépend de la classe et de la fonctionnalité de votre filtre. Pour plus d’informations, consultez [Comment les filtres connecter](how-filters-connect.md).

**Traitement et diffusion des données**

La principale fonction de la plupart des filtres consiste à traiter et à fournir des données multimédias. La façon dont cela se produit dépend du type de filtre :

-   Une source Push a un thread de travail qui remplit continuellement des exemples de données et les remet en aval.
-   Une source de tirage attend que son voisin en aval demande un échantillon. Il répond en écrivant des données dans un exemple et en livrant l’exemple au filtre en aval. Le filtre en aval crée le thread qui pilote le Data Flow.
-   Un filtre de transformation contient des exemples fournis par son voisin en amont. Lorsqu’il reçoit un exemple, il traite les données et les remet en aval.
-   Un filtre de convertisseur reçoit des exemples de en amont et les planifie pour un rendu basé sur les horodatages.

Les autres tâches liées à la diffusion en continu incluent le vidage des données du graphique, la gestion de la fin du flux et la réponse aux demandes de recherche. Pour plus d’informations sur ces problèmes, consultez les rubriques suivantes :

-   [Flow de données pour les développeurs de filtres](data-flow-for-filter-developers.md)
-   [Gestion du contrôle de la qualité](quality-control-management.md)
-   [Threads et sections critiques](threads-and-critical-sections.md)

**Prise en charge de COM**

les filtres de DirectShow sont des objets COM, généralement empaquetés dans des dll. La bibliothèque de classes de base implémente une infrastructure pour la prise en charge de COM. elle est décrite dans la section [DirectShow et COM](directshow-and-com.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[écriture de filtres de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



