---
description: Une application doit être en mesure de générer et de consommer des données à partir de plusieurs formats.
ms.assetid: bf60fab7-866b-4659-8316-653509ac5112
title: Formats de persistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8edd88a4b170d2299832a205d80dc6704aea66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296043"
---
# <a name="persistence-formats"></a>Formats de persistance

Une application doit être en mesure de générer et de consommer des données à partir de plusieurs formats. Celles-ci incluent souvent des formats binaires propriétaires et doivent également inclure des formats standard, tels que RTF (Rich Text Format) ou HTML.

Le tableau suivant répertorie certains formats qui peuvent contenir de l’encre.



| Format                                      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Binary<br/>                           | Les applications doivent utiliser le format ISF (Ink Serialized Format) pour encoder l’encre dans leurs formats binaires.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| HTML<br/>                             | Un format HTML est fortement recommandé pour la représentation d’un contenu hétérogène. Les applications doivent utiliser le format GIF (Graphics Interchange Format) viné pour encoder l’encre dans leurs documents HTML. Pour plus d’informations sur les gif enrichis, consultez [blocs de construction](building-blocks.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Image<br/>                            | Pour les applications pour lesquelles il n’existe aucune autre intersection de compatibilité, une application compatible avec l’encre doit déplacer les images au format bitmap et Metafile vers le presse-papiers.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ISF (Ink Serialized Format)<br/>      | ISF est la représentation persistante la plus compacte de l’entrée manuscrite. Bien qu’il contienne souvent uniquement des données manuscrites, ISF est extensible. Les applications peuvent définir des attributs personnalisés (identifiés par un identificateur global unique (GUID)) sur un objet [**Ink**](inkdisp-class.md) , un trait d’encre ou un point d’encre. Cela vous permet de stocker tout type de données ou métadonnées en tant qu’attribut dans un flux ISF. Pour l’interopérabilité du presse-papiers, l’encre peut être placée dans un emplacement de presse-papiers standard pour ISF défini dans les fichiers d’en-tête du kit de développement logiciel (SDK).<br/> ISF est un format spécifique à la technologie Microsoft Tablet PC et est pris en charge uniquement dans les méthodes de [**chargement**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) et d' [**enregistrement**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save) de l’objet [**Ink**](inkdisp-class.md) .<br/> |
| RTF<br/>                              | Il est possible de générer un format de presse-papiers RTF et de coder l’encre dans le format RTF en tant qu’objets OLE. cela permet le collage de l’encre dans un conteneur OLE, par exemple Microsoft Word ou une application basée sur RichEdit.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| XML (Extensible Markup Language)<br/> | Les applications peuvent utiliser l’un des formats d’encre de base-64 codés pour stocker l’encre dans un format de fichier XML. Un format XML est utile pour entrer du contenu manuscrit dans une base de données, comme dans le cas d’un champ de signature, ou même en tant que format de fichier principal des applications. Cela évite d’avoir à écrire un analyseur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

 

 




