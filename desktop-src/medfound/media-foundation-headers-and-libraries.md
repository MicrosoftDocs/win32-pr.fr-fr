---
description: Cette rubrique répertorie les en-têtes et les bibliothèques qui définissent toutes les API Media Foundation.
ms.assetid: 69877842-fafe-408f-b55b-d2ff2277c756
title: Media Foundation en-têtes et bibliothèques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6db7650c98f6491fa6db4010273475b4bd103a2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467466"
---
# <a name="media-foundation-headers-and-libraries"></a>Media Foundation en-têtes et bibliothèques

Cette rubrique répertorie les en-têtes et les bibliothèques qui définissent toutes les API Media Foundation.

Pour trouver l’en-tête et la bibliothèque d’un élément d’API spécifique, consultez les pages de référence dans le [Media Foundation référence de programmation](media-foundation-programming-reference.md).

## <a name="headers"></a>En-têtes

-   codecapi. h
-   d3d11. h
-   d3d9. h
-   d3d9caps. h
-   d3d9types. h
-   DXVA. h
-   dxva2api. h
-   dxvahd. h
-   evr. h
-   evr9. h
-   mfapi. h
-   mfcaptureengine. h
-   mferrors. h
-   mfidl. h
-   mfmediacapture. h
-   mfmediaengine. h
-   mfmp2dlna. h
-   mfobjects. h
-   mfplat. lib
-   mfplay. h
-   mfreadwrite. h
-   mftransform. h
-   opmapi. h
-   wmcodecdsp. h
-   wmcontainer. h

## <a name="libraries"></a>Bibliothèques

-   dxva2. lib
-   evr. lib
-   MF. lib
-   mfplat. lib
-   mfplay. lib
-   mfreadwrite. lib
-   mfuuid. lib

## <a name="library-changes-in-windows-7"></a>modifications de la bibliothèque dans Windows 7

à partir de Windows 7, certaines fonctions Media Foundation sont exportées à partir de fichiers DLL différents de ceux des versions précédentes.

Ces modifications affectent les fichiers. lib suivants :

-   evr. lib
-   MF. lib
-   mfplat. lib

Une application qui utilise l’une de ces fonctions doit être liée à un autre jeu de fichiers. lib, en fonction de la version du kit de développement logiciel (SDK) et de la plateforme cible.




| Version du SDK | Bibliothèques | 
|-------------|-----------|
| Windows kit de développement logiciel pour Windows Vista<br /> Windows kit de développement logiciel (SDK) pour Windows Server 2008<br /> | evr. lib<br /> MF. lib<br /> mfplat. lib<br /> | 
| Windows SDK pour Windows 7 | si la plateforme cible est Windows Vista ou Windows Server 2008, liez les bibliothèques suivantes :<br /><ul><li>evr_vista. lib</li><li>mf_vista. lib</li><li>mfplat_vista. lib</li></ul>si la plateforme cible est Windows 7 ou version ultérieure, liez les bibliothèques suivantes :<br /><ul><li>evr. lib</li><li>MF. lib</li><li>mfplat. lib</li></ul> | 




 

## <a name="additional-info-on-helper-functions"></a>Informations supplémentaires sur les fonctions d’assistance

le Windows 8 MFPlat.dll est un composant du système d’exploitation Microsoft Windows. Il comporte plusieurs fonctions incluses dans le module.

MFPlat implémente la fonctionnalité d’assistance pour l’allocation de mémoire de bas niveau, les FIFO de planification des opérations et les abstractions d’accès aux fichiers Win32. Pour être plus précis, il prend en charge les éléments suivants :

-   allouer et initialiser des mémoires tampons (appelées « exemples ») et des applications auxiliaires pour simplifier la gestion de leurs durées de vie
-   fonctions efficaces de copie des données pour les mémoires tampons
-   allocation et initialisation des FIFO d’opération (appelées « Events »)
-   implémentation d’un objet horloge simple
-   implémentation d’un wrapper de fichier Win32
-   allocation et initialisation de tableaux de mémoires tampons pour les processeurs et les GPU

Si la méthode [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) est réussie, MFPlat fournit les fonctionnalités de file d’attente de travail suivantes :

-   prise en charge interne des éléments d’e/s (utilisés par le wrapper de fichier Win32 et les bibliothèques de Sockets)
-   fourniture d’un tableau de files d’attente de travail multithread avec prise en charge de la priorité des threads
-   prise en charge des éléments de travail, des éléments de minuteur et des éléments d’attente via les files d’attente de travail

MFPlat fournit une fonctionnalité d’assistance pour la recherche et la création de transformations multimédias et de sources de média enregistrées sur le système, ainsi que la création et la manipulation de types de médias, bien que MFPlat lui-même ne puisse pas créer le média réel ni le lire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de Media Foundation](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 




