---
description: Les services de ligne étendus (ou services de ligne spécifiques au périphérique) incluent toutes les extensions définies par le fournisseur de services pour l’API.
ms.assetid: 0f01509e-caa5-4f79-be78-36bd5f23c5d7
title: Fonctions de ligne étendues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 394ad011a5752a45f82de4934a3f87c9f1590870b245fdc113f57badb4298290
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003657"
---
# <a name="extended-line-functions"></a>Fonctions de ligne étendues

Les services de ligne étendus (ou services de ligne spécifiques au périphérique) incluent toutes les extensions définies par le fournisseur de services pour l’API. L’API définit un mécanisme qui permet aux fournisseurs de fournisseurs de services d’étendre l’interface TAPI à l’aide d’extensions spécifiques à l’appareil. L’API définit uniquement le mécanisme d’extension, ce qui permet d’accéder aux extensions spécifiques à l’appareil, mais l’API ne définit pas leur comportement. Le comportement est entièrement défini par le fournisseur de services.

L’interface TAPI est constituée de définitions de constantes scalaires et binaires, de structures de données, de fonctions et de messages. Les procédures définies permettent à un fournisseur d’étendre la plupart de ces méthodes comme suit.

Pour les constantes de données scalaires extensible, un fournisseur de fournisseurs de services peut définir de nouvelles valeurs dans une plage spécifiée. Étant donné que la plupart des constantes de données sont des **DWORD** s, en général, la plage comprise entre 0X00000000 et 0x7FFFFFFF est réservée aux extensions futures courantes, tandis que 0X80000000 à 0xFFFFFFFF sont disponibles pour les extensions spécifiques au fournisseur. L’hypothèse est qu’un fournisseur définit des valeurs qui sont des extensions naturelles des types de données définis par l’API.

Pour les constantes de données de l’indicateur de bit extensible, un fournisseur de fournisseurs de services peut définir de nouvelles valeurs pour les bits spécifiés. Comme la plupart des constantes d’indicateur de bit sont des **DWORD** s, un nombre spécifique de bits inférieurs est réservé pour les extensions communes, tandis que les bits supérieurs restants sont disponibles pour les extensions spécifiques au fournisseur. Les indicateurs binaires communs sont assignés de bit zéro vers le haut ; les extensions spécifiques au fournisseur doivent être affectées de bit 31. Cela offre une flexibilité maximale pour assigner des positions de bits aux extensions communes et aux extensions spécifiques au fournisseur. Un fournisseur est censé définir de nouvelles valeurs qui sont des extensions naturelles des indicateurs binaires définis par l’API.

Les structures de données extensibles ont un champ de taille variable qui est réservé à une utilisation spécifique à l’appareil. Une taille variable, le fournisseur de services décide de la quantité d’informations et de l’interprétation. Un fournisseur qui définit un champ spécifique à l’appareil est supposé créer ces extensions naturelles de la structure de données d’origine définies par l’API.

Deux fonctions, [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) et [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature), et deux messages associés, [**line \_ DEVSPECIFIC**](line-devspecific.md) et [**line \_ DEVSPECIFICFEATURE**](line-devspecificfeature.md), fournissent un mécanisme d’extension spécifique au fournisseur. La fonction **lineDevSpecific** et le message DEVSPECIFIC de ligne associé \_ permettent à une application d’accéder à des fonctionnalités de ligne, d’adresse ou d’appel spécifiques à l’appareil qui ne sont pas disponibles avec les services de téléphonie de base ou supplémentaires. Le profil de paramètre de la fonction **lineDevSpecific** est générique dans le fait que peu d’interprétation des paramètres est effectuée par l’API. L’interprétation des paramètres est définie par le fournisseur de services et doit être comprise par une application qui les utilise. Les paramètres sont simplement transmis par le biais de l’interface TAPI de l’application au fournisseur de services. Une application qui s’appuie sur des extensions spécifiques à l’appareil ne fonctionne généralement pas avec d’autres fournisseurs de services ; Toutefois, les applications écrites dans les services de téléphonie de base et supplémentaires fonctionnent avec le fournisseur de services étendu.

Pour plus de commodité, une fonction d’échappement plus spécialisée est également fournie. Il est similaire à [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific), mais il place l’interprétation sur certains paramètres. Cette fonction plus spécialisée est [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature), une fonction d’échappement spécifique à l’appareil qui permet d’envoyer des fonctionnalités de commutation au commutateur. La ligne de message [**\_ DEVSPECIFICFEATURE**](line-devspecificfeature.md) est le message spécifique à l’appareil envoyé à l’application en tant qu’indication des fonctionnalités envoyées au commutateur. Cette fonction et son message associé permettent à une application d’émuler des enfoncements de bouton sur le téléphone de fonctionnalité de la ligne. Comme les téléphones de caractéristiques et les significations de leurs boutons sont spécifiques au fournisseur, l’appel de fonctionnalités à l’aide de [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) est également spécifique au fournisseur.

Comme mentionné précédemment, il n’existe pas de registre central pour les identificateurs de fabricant. Au lieu de cela, un générateur d’identificateur unique (EXTIDGEN) est mis à disposition.

 

 



