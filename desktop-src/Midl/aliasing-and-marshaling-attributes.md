---
title: Attributs d’alias et de marshaling
description: Les applications distribuées passent presque toujours des données entre les programmes client et serveur lorsqu’elles appellent des procédures d’interface.
ms.assetid: 64895c64-f16b-47c4-928d-5149808b0476
keywords:
- IDL MIDL, attributs MIDL, crénelage et marshaling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ac66aa04210a878c67ee6bcf1a50ff21fa1d1d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093802"
---
# <a name="aliasing-and-marshaling-attributes"></a>Attributs d’alias et de marshaling

Les applications distribuées passent presque toujours des données entre les programmes client et serveur lorsqu’elles appellent des procédures d’interface. Les développeurs utilisent MIDL pour décrire les données que les programmes client et serveur transmettent de manière standard. Le compilateur MIDL crée des programmes stub d’application, ou proxy, pour le client et le serveur qui convertissent les données en un format standardisé pouvant être envoyé sur un réseau. Ce format, le format de représentation de données réseau (NDR), est souvent appelé le format de transmission des données. Les stubs doivent convertir les données à partir de leur format natif dans l’espace mémoire du programme vers NDR. Cette conversion est appelée marshaling des données. Lorsqu’un client ou un programme serveur reçoit des données, il doit convertir les données du rapport de non-remise au format natif de ce programme. C’est ce que l’on appelle démarshaler les données.

Utilisez des attributs d’alias et de marshaling pour contrôler la façon dont vos données sont empaquetées dans un format de rapport de non-remise et transmises sur le réseau.



| Attribut                             | Usage                                                                                                                         |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**appeler \_ en tant que**](call-as.md)           | Cartes une fonction qui n’est pas accessible à distance à un appel de procédure distante.                                                                      |
| [**IID \_ est**](iid-is.md)             | Fournit l’identificateur d’interface de l’interface COM qui est l’objet du pointeur.                                     |
| [**transmettre \_ en tant que**](transmit-as.md)   | Convertit un type de données en un type plus simple pour la transmission sur un réseau.                                                       |
| [**Marshal de câble \_**](wire-marshal.md) | Semblable à [**transmit \_ As**](transmit-as.md) , mais vous implémentez les routines de dimensionnement, de marshaler, de démarshaler et de libération des données. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conversion de type et marshaling des attributs ACF](type-conversion-and-marshaling-acf-attributes.md)
</dt> </dl>

 

 




