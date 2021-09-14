---
description: Exemple de filtre InfTee
ms.assetid: ba401528-9706-41fb-99d1-2bc3ffc05f1a
title: Exemple de filtre InfTee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd0fc5a1d550e0327da0d0d3dd47c8847ffafee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126853749"
---
# <a name="inftee-filter-sample"></a>Exemple de filtre InfTee

## <a name="description"></a>Description

le filtre InfTee fournit un exemple d’implémentation de la DirectShow filtre [Tee de code Pin infini](infinite-pin-tee-filter.md) . Le filtre a une broche d’entrée et un nombre dynamique de broches de sortie. Tous les exemples de supports envoyés au filtre sont remis simultanément à partir de toutes les broches de sortie.

Ce filtre apparaît dans GraphEdit sous le nom « sample infini pin tee » pour le distinguer du filtre tee de code confidentiel infini standard fourni dans DirectShow.

## <a name="usage"></a>Usage

Étant donné que ce filtre ne modifie pas les données qu’il reçoit, tous les codes confidentiels doivent accepter le même type de média. Pendant le processus de connexion, le filtre peut reconnecter certains codes confidentiels pour que les types de média correspondent.

Les données arrivant à la broche d’entrée ne sont pas copiées avant d’être envoyées aux broches de sortie. Le filtre garantit également que les données sont remises aux filtres en aval, pour garantir que les deux sorties reçoivent le service en temps opportun. En particulier, si l’une des sorties peut se bloquer dans la fonction membre [**COutputQueue :: Receive**](coutputqueue-receive.md) , l’tee crée un thread pour remettre l’exemple. S’il n’existait aucun thread pour remettre l’exemple, le thread qui remet l’échantillon à la broche d’entrée tee peut passer les données à un filtre en aval ; à ce stade, il peut bloquer, en conservant les données de l’autre filtre en aval pendant de longues périodes.

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

cet exemple est installé sous le chemin d’accès suivant : exemples *\[ racine \] du kit de développement logiciel (SDK)* \\ \\ \\ \\ InfTee filtres de DirectShow \\ .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Extraits](directshow-samples.md)
</dt> </dl>

 

 



