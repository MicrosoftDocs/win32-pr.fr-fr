---
description: Utilisation de l’exclusion mutuelle pour les Flux ASF
ms.assetid: fdd31eac-1dd6-45f0-90fb-d5a74c85db2e
title: Utilisation de l’exclusion mutuelle pour les Flux ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411b5aa0638ab1c56298b93d01e8de99920abc6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412884"
---
# <a name="using-mutual-exclusion-for-asf-streams"></a>Utilisation de l’exclusion mutuelle pour les Flux ASF

Le contenu ASF peut contenir plusieurs flux qui s’excluent mutuellement. Ces flux ne peuvent pas être lus simultanément, mais un seul d’entre eux est lu à la fois. Par exemple, le fichier peut contenir un ensemble de flux qui comprend le même contenu encodé à une vitesse de transmission différente. Le flux utilisé est déterminé par la bande passante disponible pour l’application qui diffuse le contenu. L’objet exclusion mutuelle ASF, qui fait partie de l’objet d’en-tête, stocke des informations sur le groupe de flux de données qui s’excluent mutuellement.

Dans Media Foundation, l’objet *exclusion mutuelle* qui expose l’interface [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) existe pour chaque objet exclusion mutuelle ASF. L’objet profil contient une référence à tous les objets d’exclusion mutuelle.

L’objet exclusion mutuelle stocke les informations sur le groupe de flux s’excluant mutuellement sous forme d’enregistrements. Un objet d’exclusion mutuelle peut avoir plusieurs enregistrements qui peuvent être utilisés pour créer des scénarios complexes. Chaque enregistrement contient un ou plusieurs flux qui ne peuvent pas coexister avec des flux dans un autre enregistrement, géré par l’objet exclusion mutuelle, en fonction du type d’exclusion mutuelle, tel que la vitesse de transmission.

Un exemple courant d’exclusion mutuelle complexe est un fichier qui contient trois flux audio du même contenu à différentes vitesses de transmission dans chacune des trois langues. Seul l’un des neuf flux doit être lu à la fois, mais il existe deux types par lesquels ils s’excluent mutuellement : le langage et la vitesse de transmission.

Pour cet exemple, les neuf flux reçoivent les numéros de flux suivants :

<dl> 1-langue 1, taux de bits 1  
2-langage 1, taux de bits 2  
3 langues 1, taux de bits 3  
4-langue 2, taux de bits 1  
5 langues 2, débit binaire 2  
6 langues 2, débit binaire 3  
7-langue 3, taux de bits 1  
8 langues 3, taux de bits 2  
9-langage 3, débit binaire 3  
</dl>

Ce scénario peut être implémenté à l’aide des quatre objets d’exclusion mutuelle suivants :

-   Le premier objet d’exclusion mutuelle comprend les flux 1, 2 et 3, qui sont mutuellement exclusifs par vitesse de transmission. Chaque flux a son propre enregistrement.
-   Le deuxième objet d’exclusion mutuelle comprend les flux 4, 5 et 6, qui s’excluent mutuellement par vitesse de transmission. Chaque flux a son propre enregistrement.
-   Le troisième objet d’exclusion mutuelle comprend 7, 8 et 9, et s’exclut mutuellement par vitesse de transmission. Chaque flux a son propre enregistrement.
-   Le quatrième objet d’exclusion mutuelle contient trois enregistrements, le premier incluant les flux 1, 2 et 3. la seconde, y compris les flux 4, 5 et 6 ; et le troisième, y compris les flux 7, 8 et 9. Ces enregistrements sont mutuellement exclusifs par langue.

Lors de la lecture d’un fichier créé de cette façon, l’application de diffusion en continu sélectionne la langue en premier, car elle est moins susceptible de changer au milieu de la présentation, puis de sélectionner une vitesse de transmission.

## <a name="mutual-exclusion-object-creation-and-configuration"></a>Création et configuration d’objets d’exclusion mutuelle

La liste suivante résume le processus de configuration d’un objet d’exclusion mutuelle :

1.  Créez un objet d’exclusion mutuelle.
2.  Définissez le type d’exclusion mutuelle.
3.  Configurez l’objet exclusion mutuelle en ajoutant des enregistrements et les flux associés.
4.  Ajoutez l’objet exclusion mutuelle au profil.

Pour créer et configurer un objet d’exclusion mutuelle

1.  Appelez [**IMFASFProfile :: CreateMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createmutualexclusion) pour créer un objet d’exclusion mutuelle vide.
2.  Appelez [**IMFASFMutualExclusion :: setType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype) pour définir le critère du flux s’excluant mutuellement.

    Les flux peuvent être mutuellement exclusifs par langue, vitesse de transmission, présentation et critère personnalisé. Le type est représenté sous la forme d’un GUID. Pour obtenir la liste de ces constantes, consultez [GUID de type d’exclusion mutuelle ASF](asf-mutual-exclusion-type-guids.md).

3.  Appelez [**IMFASFMutualExclusion :: AddRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addrecord) pour ajouter un enregistrement à l’objet exclusion mutuelle.

    Cette méthode ajoute un enregistrement vide et lui attribue un index d’enregistrement commençant à zéro.

4.  Appelez [**IMFASFMutualExclusion :: AddStreamForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addstreamforrecord) pour ajouter le numéro de flux à l’enregistrement spécifié par l’index d’enregistrement.

    Chaque enregistrement comprend un ou plusieurs flux. Chaque flux d’un enregistrement s’exclut mutuellement de tous les flux dans tous les autres enregistrements. Pour obtenir le nombre de flux dans un enregistrement, appelez [**IMFASFMutualExclusion :: GetStreamsForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord) en spécifiant l’index d’enregistrement.

    Pour supprimer un flux de l’enregistrement, appelez [**IMFASFMutualExclusion :: RemoveStreamFromRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removestreamfromrecord) et spécifiez l’index d’enregistrement et le numéro de flux.

5.  Appelez [**IMFASFProfile :: AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) pour ajouter l’objet exclusion mutuelle configurée au profil.

## <a name="enumerating-mutual-exclusion-objects-in-a-profile"></a>Énumération d’objets d’exclusion mutuelle dans un profil

Si [**IMFASFProfile :: AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) s’exécute correctement, il assigne un index à l’objet spécifié, en commençant à zéro.

Pour énumérer les objets d’exclusion mutuelle associés à un profil, appelez [**IMFASFProfile :: GetMutualExclusionCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount) et parcourez la liste en appelant [**IMFASFProfile :: GetMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusion). Les index d’exclusion mutuelle sont séquentiels et sont compris entre 0 et un de moins que le nombre de flux récupérés par **GetMutualExclusionCount**.

Un objet d’exclusion mutuelle est supprimé du profil en appelant [**IMFASFProfile :: RemoveMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion). Le profil réaffecte les index d’exclusion mutuelle afin qu’ils soient séquentiels à partir de zéro. Cela remplace les index précédemment stockés, qui ne sont plus valides après l’appel de cette méthode. Cela libère les enregistrements de flux d’exclusion mutuelle associés.

## <a name="removing-records-in-a-mutual-exclusion-object"></a>Suppression d’enregistrements dans un objet d’exclusion mutuelle

Pour supprimer un enregistrement d’un objet d’exclusion mutuelle, appelez [**IMFASFMutualExclusion :: RemoveRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removerecord). Si cette méthode est réussie, l’objet exclusion mutuelle indexe les enregistrements restants afin qu’ils soient séquentiels à partir de zéro. L’application doit énumérer les enregistrements pour garantir l’index correct pour chaque enregistrement. Pour ce faire, appelez [**IMFASFMutualExclusion :: GetRecordCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getrecordcount) et parcourez les enregistrements en appelant [**IMFASFMutualExclusion :: GetStreamsForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord).

La suppression de l’enregistrement avec l’index le plus élevé n’a aucun effet sur les autres index.

## <a name="modifying-a-mutual-exclusion-object"></a>Modification d’un objet d’exclusion mutuelle

Pour modifier la configuration de l’objet exclusion mutuelle dans le profil, l’application doit remplacer l’objet exclusion mutuelle existant par un autre objet qui contient les nouveaux paramètres.

Pour modifier la configuration de l’objet exclusion mutuelle dans le profil

1.  Énumérez les objets d’exclusion mutuelle dans le profil pour récupérer l’objet qui doit être modifié.
2.  Appelez [**IMFASFMutualExclusion :: Clone**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-clone) pour cloner l’objet exclusion mutuelle.

3.  Configurez l’objet cloné si nécessaire.
4.  Appelez [**IMFASFProfile :: RemoveMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion) pour supprimer l’ancien objet exclusion mutuelle du profil.

5.  Appelez [**IMFASFProfile :: AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) pour ajouter l’objet d’exclusion mutuelle mis à jour au profil.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Profil ASF](asf-profile.md)
</dt> </dl>

 

 



