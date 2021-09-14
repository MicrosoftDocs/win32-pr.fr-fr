---
title: Documents et périphériques de document
description: Windows 7 offre aux développeurs une plate-forme robuste pour travailler avec des documents et intégrer des périphériques de document.
ms.assetid: 77d27775-eea8-4739-a1d2-05fcf6590cef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e220949d37c17b95f92ed5026166ea71043354
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293202"
---
# <a name="documents-and-document-peripherals"></a>Documents et périphériques de document

Windows 7 offre aux développeurs une plate-forme robuste pour travailler avec des documents et intégrer des périphériques de document. deux nouvelles technologies de documents et de stockage ont été introduites dans Windows Vista : XML Paper Specification (XPS) et Open Packaging Conventions (OPC). ces technologies, qui étaient disponibles dans Windows Vista uniquement aux développeurs d’applications de code géré par le biais de Microsoft .NET Framework, sont désormais disponibles dans le kit de développement logiciel (SDK) Windows 7software pour une utilisation par les développeurs de code non managé.

## <a name="open-packaging-conventions"></a>Open Packaging Conventions

Windows 7 prend en charge tous les formats de fichier OPC, y compris ceux de Microsoft, ainsi que ceux des tiers. OPC est un composant de la spécification internationale OOXML Open XML () défini par Office l’intermédiaire des normes *ISO/IEC DIS 29500* et *ECMA-376*. Basé sur le format de fichier *zip* , OPC permet aux applications de stocker une combinaison d’éléments de données dans un seul fichier de package. les développeurs d’applications peuvent utiliser les api de *Packaging* dans Windows 7 pour créer, lire et manipuler plusieurs éléments de données dans des fichiers OPC.

à l’aide des api de *Packaging* dans Windows 7, les développeurs peuvent créer de nouveaux formats de package pour répondre aux besoins de stockage de données propres à l’application.

Les signatures numériques *x509* sont également prises en charge par les API de *Packaging*. Les développeurs peuvent utiliser les fonctionnalités de signature numérique pour signer et valider les parties sélectionnées d’un package OPC ou de l’ensemble du package. Les applications peuvent attribuer à leurs documents un niveau de sécurité supplémentaire en utilisant des signatures numériques pour détecter quand le contenu d’un fichier OPC a été modifié après la signature du fichier. (Consultez la [vue d’ensemble des conventions Open Packaging](/previous-versions/windows/desktop/opc/open-packaging-conventions-overview).)

## <a name="xps-documents"></a>Documents XPS

les développeurs d’applications Windows peuvent créer des applications qui produisent des documents XPS avec Windows 7. Cela leur permet de s’intégrer étroitement à l’écosystème de périphériques du document (des appareils tels que les scanneurs et les imprimantes) et d’utiliser du papier électronique sécurisé pour prendre en charge la publication et l’archivage.

dans les versions précédentes de Windows, XPS n’était pas pris en charge pour les développeurs Microsoft Win32. XPS a été introduit dans Windows Vista, mais la surface de l’API était limitée aux développeurs .net qui utilisaient du code géré. avec Windows 7, les développeurs Win32 peuvent utiliser les nouvelles api de *Document* xps pour réduire la quantité de travail requise lors de l’utilisation d’xps. étant donné que XPS est la base de la nouvelle plate-forme d’impression Windows, il s’agit d’un avantage significatif.

dans les versions précédentes de Windows, l’accès au chemin d’impression XPS à partir des applications Win32 était limité aux séquences d’échappement du pilote. Cela a considérablement réduit l’utilitaire du chemin d’impression pour les développeurs qui n’utilisent pas de code managé. Pour les développeurs Win32, la nouvelle API d'*impression* XPS réduit considérablement la quantité de travail requise pour tirer parti des avantages du chemin d’impression XPS et élimine le besoin de code d’impression parallèle.

Les développeurs d’applications peuvent utiliser des documents XPS pour partager et archiver du contenu sous forme de document électronique dans un format fiable, efficace et fiable. tout comme Windows Vista, le chemin d’impression dans Windows 7 est basé sur le format XPS pour offrir des fonctionnalités d’impression améliorées. les api de document xps dans Windows 7 offrent aux développeurs la possibilité de créer, d’accéder et de manipuler facilement des documents XPS. (Consultez le [Guide de programmation de documents XPS](/previous-versions//dd372978(v=vs.85)).)

![Visionneuse XPS](images/windows7-devguide-xpsviewer.jpg)

les développeurs d’applications Windows peuvent créer des applications qui produisent des documents XPS avec Windows 7

 

 