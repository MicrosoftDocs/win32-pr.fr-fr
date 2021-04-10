---
description: Exemple DMOEnum
ms.assetid: afd7853e-b0ab-42f6-8c2e-c2b0b40d989b
title: Exemple DMOEnum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c413b7787ba12785758cffed89be15229373643d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200819"
---
# <a name="dmoenum-sample"></a>Exemple DMOEnum

## <a name="description"></a>Description

Cet exemple d’application énumère tous les objets DMOs ( [DirectX Media Objects](directx-media-objects.md) ) inscrits dans le système de l’utilisateur et affiche des informations à leur sujet.

L’exemple utilise la fonction [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) et l’interface [**IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) pour énumérer le DMOs. Elle utilise l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) et d’autres interfaces DMO pour récupérer des informations sur chaque DMO.

## <a name="usage"></a>Utilisation

Lorsque l’application démarre, elle énumère tous les DMOs installés. Si vous sélectionnez une catégorie DMO spécifique, l’application affiche uniquement les DMOs dans cette catégorie. Pour afficher des informations sur un DMO, sélectionnez DMO dans la liste. L’application affiche le nombre de flux, les types de médias préférés, le serveur DLL pour cette solution DMO et d’autres informations sur la solution DMO. Pour inclure ou exclure des DMOs à clé, activez la case à cocher **inclure les DMOs de clé** .

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Cet exemple est installé sous le chemin d’accès suivant : exemples *\[ racine \] du kit de développement logiciel (SDK)* \\ \\ \\ DirectShow \\ divers \\ DMOEnum.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples DirectShow](directshow-samples.md)
</dt> </dl>

 

 



