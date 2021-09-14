---
description: Exemple DMOEnum
ms.assetid: afd7853e-b0ab-42f6-8c2e-c2b0b40d989b
title: Exemple DMOEnum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c413b7787ba12785758cffed89be15229373643d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324914"
---
# <a name="dmoenum-sample"></a>Exemple DMOEnum

## <a name="description"></a>Description

Cet exemple d’application énumère tous les objets DMOs ( [DirectX Media Objects](directx-media-objects.md) ) inscrits dans le système de l’utilisateur et affiche des informations à leur sujet.

L’exemple utilise la fonction [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) et l’interface [**IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) pour énumérer le DMOs. elle utilise l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) et d’autres interfaces de DMO pour récupérer des informations sur chaque DMO.

## <a name="usage"></a>Usage

Lorsque l’application démarre, elle énumère tous les DMOs installés. si vous sélectionnez une catégorie de DMO spécifique, l’application affiche uniquement les DMOs dans cette catégorie. pour afficher des informations sur un DMO, sélectionnez l’DMO dans la liste. l’application affiche le nombre de flux, les types de médias préférés, le serveur DLL pour ce DMO et d’autres informations sur le DMO. Pour inclure ou exclure des DMOs à clé, activez la case à cocher **inclure les DMOs de clé** .

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

cet exemple est installé sous le chemin d’accès suivant : exemples *\[ racine \] SDK* \\ \\ \\ DirectShow \\ divers \\ DMOEnum.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Extraits](directshow-samples.md)
</dt> </dl>

 

 



