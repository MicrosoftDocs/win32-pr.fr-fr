---
description: à partir de Windows 7, Windows Management Instrumentation (WMI) implémentait un mécanisme standard pour la découverte des profils à l’aide du schéma CIM.
ms.assetid: e748b623-5ff3-464d-ba09-96cf226de7b6
ms.tgt_platform: multiple
title: Traversée d’association entre espaces de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe2bbb408c4d89a7093adf45f3daf276df294ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127526225"
---
# <a name="cross-namespace-association-traversal"></a>Traversée d’association entre espaces de noms

à partir de Windows 7, Windows Management Instrumentation (WMI) implémentait un mécanisme standard pour la découverte des profils à l’aide du schéma CIM.

WMI prend en charge l’inscription des profils d’association et de parcours d’association entre espaces de noms. Pour plus d’informations sur l’inscription des profils et l’implémentation standard CIM de la traversée d’association, consultez DSP1033 ( [https://www.dmtf.org/standards/published\_documents/DSP1033.pdf](https://www.dmtf.org/sites/default/files/standards/documents/DSP1033_1.0.0.pdf) )

Pour prendre en charge cette fonctionnalité, l’infrastructure WMI a effectué les opérations suivantes :

-   Création de l’espace de noms Interop : \\ \\ Interop racine.
-   Traversée des associations entre espaces de noms autorisées. Les associations qui traversent des espaces de noms prennent en charge le filtrage au niveau de la classe d’association et au niveau de l’espace de noms implémenté.
-   Ajout des classes [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)), [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)et [**CIM \_ ReferencedProfile**](cim-referencedprofile.md) .
-   Mise en œuvre de la version du schéma CIM compatibilité 2.17.1. Pour plus d’informations, consultez [compatibilité du schéma CIM](cim-schema-compatibility.md).

## <a name="interop-namespace"></a>Espace de noms Interop

L’espace de noms Interop fournit un emplacement commun pour qu’une application cliente Découvre tous les profils pris en charge sur un ordinateur. Les profils peuvent être utilisés pour gérer différents aspects d’un système d’exploitation, d’un groupe de stockage ou d’une base de données.

Tous les objets et classes Interop doivent être définis dans l' \\ espace de noms Interop racine.

## <a name="cim-classes"></a>Classes CIM

Les classes CIM décrites dans la liste suivante prennent en charge la traversée d’association entre espaces de noms.

<dl> <dt>

<span id="CIM_RegisteredProfile"></span><span id="cim_registeredprofile"></span><span id="CIM_REGISTEREDPROFILE"></span>[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))
</dt> <dd>

Utilisé pour identifier la spécification de profil publiée comme étant implémentée. Cette classe spécifie les informations qui incluent le nom du profil, l’organisation et la version avec lesquelles l’implémentation est conforme.

</dd> <dt>

<span id="CIM_ElementConformsToProfile"></span><span id="cim_elementconformstoprofile"></span><span id="CIM_ELEMENTCONFORMSTOPROFILE"></span>[**\_ELEMENTCONFORMSTOPROFILE CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dd>

Utilisé pour associer des instances d’éléments de gestion définis dans des profils à la classe [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) qui identifie les spécifications de profil spécifiques qui sont implémentées.

</dd> <dt>

<span id="CIM_ReferencedProfile"></span><span id="cim_referencedprofile"></span><span id="CIM_REFERENCEDPROFILE"></span>[**\_REFERENCEDPROFILE CIM**](cim-referencedprofile.md)
</dt> <dd>

Utilisé pour représenter la relation entre les profils.

</dd> </dl>

## <a name="implementing-cross-namespace-association-traversal"></a>Implémentation du parcours des associations entre espaces de noms

Le service WMI autorise le parcours de l’association entre espaces de noms. WMI fournit l’espace de noms Interop pour inscrire des profils et les associer aux profils qui sont implémentés dans différents espaces de noms. Toutefois, pour utiliser le parcours d’association, les implémenteurs doivent instancier les classes de profil dans l’interopérabilité et dans l’espace de noms implémenté. Pour plus d’informations, consultez [écriture d’un fournisseur d’associations pour l’interopérabilité](writing-an-association-provider-for-interop.md).

Les associations qui traversent des espaces de noms dans le même environnement de gestion doivent être instanciées à la fois dans les espaces de noms Interop et Implemented. Dans le cas contraire, la traversée d’association ne fonctionnera pas. Par exemple, le fournisseur d’associations Power profile doit être inscrit avec les espaces de noms root/Interop et root/cimv2/Power. La traversée d’association doit pouvoir se produire à partir de l’espace de noms vers l’autre. Pour obtenir des exemples de parcours d’association, consultez [accès aux données dans l’espace de noms Interop](accessing-data-in-the-interop-namespace.md).

* * Windows Vista : * *

après la mise à niveau vers Windows 7, si des profils d’appareils d’interopérabilité étaient précédemment installés dans l’espace de noms racine/interop, aucun profil Windows 7 n’est installé. ces objets de profil tiers remplacent le schéma d’interopérabilité Windows 7 pour gérer les fonctionnalités. En outre, l’ID d’événement 5631 de l’application WMI est enregistré.

pour récupérer les profils d’interopérabilité Windows 7, la version Windows 7 du fichier interop. mof et les fichiers MFL associés doivent être compilés. Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[**\_ELEMENTCONFORMSTOPROFILE CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[**\_REFERENCEDPROFILE CIM**](cim-referencedprofile.md)
</dt> <dt>

[Compatibilité du schéma CIM](cim-schema-compatibility.md)
</dt> <dt>

[Écriture d’un fournisseur d’association pour l’interopérabilité](writing-an-association-provider-for-interop.md)
</dt> <dt>

[Accès aux données dans l’espace de noms Interop](accessing-data-in-the-interop-namespace.md)
</dt> </dl>

 

 
