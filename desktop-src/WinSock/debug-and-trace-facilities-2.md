---
description: Fonctionnalités de débogage et de suivi et Windows Sockets 2.
ms.assetid: eb29fc21-92d6-4471-860a-fd1c531686f6
title: Fonctionnalités de débogage et de suivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7288c6b4d72a7a375ee16da23a25b0a04a46df91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515242"
---
# <a name="debug-and-trace-facilities"></a>Fonctionnalités de débogage et de suivi

Les développeurs d’applications Windows Sockets 2 doivent isoler les bogues dans :

-   Application.
-   *Ws2 \_32.dll* ou l’une des dll de shim de compatibilité.
-   Fournisseur de services.

Windows Sockets 2 répond à ce besoin par le biais de plusieurs composants et fonctionnalités :

-   Prise en charge intégrée du suivi Winsock sur Windows Vista et versions ultérieures.
-   Une version de débogage spécialement conçue de *la \_32.dllWs2* sur Windows Vista.
-   Une fonctionnalité de débogage et de traçage primitive distincte pour une utilisation sur Windows Server 2003 et Windows XP.

## <a name="winsock-tracing-using-event-tracing-for-windows"></a>Suivi Winsock à l’aide de Suivi d’v nements pour Windows

La prise en charge intégrée du suivi Winsock à l’aide d’Suivi d’v nements pour Windows (ETW) est incluse sur Windows Vista et versions ultérieures. Il s’agit de la méthode recommandée pour le suivi des appels Winsock sur Windows Vista et versions ultérieures. Le suivi Winsock à l’aide d’ETW est léger et fonctionne sur les versions commerciales de Windows. Aucun logiciel ou composant supplémentaire n’est requis. Cette fonctionnalité doit simplement être activée sur Windows Vista et versions ultérieures. Pour plus d’informations, consultez les rubriques de [suivi Winsock](winsock-tracing.md) .

## <a name="using-a-debug-version-of-ws2_32dll"></a>Utilisation d’une version de débogage de Ws2 \_32.dll

La combinaison d’une version de débogage de la *\_32.dllWs2* sur Windows Vista et le suivi Winsock permet d’analyser tous les appels de procédure sur l’API Windows Sockets 2 ou SPI et, dans une certaine mesure, contrôlés.

Si une version du kit de développement logiciel (SDK) Microsoft Windows pour Windows Vista est installée à l’emplacement par défaut, les versions Debug de la *\_32.dllWs2* pour différentes architectures se trouvent dans le dossier suivant :

**C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 6.0 \\ noredimst**

Une version vérifiée de *l' \_32.dllWs2* qui correspond à la version de Windows et au Service Pack sur lequel vous effectuez le test doit être utilisée. Sachez que des correctifs de sécurité ont peut-être été appliqués et mis à jour le *\_32.dllWs2* sur votre système de test. La SDK Windows pour Windows Vista et les anciens abonnements de DVD/CD du kit de développement logiciel (SDK) de la plateforme précédente incluent les builds vérifiées pour les différentes versions de Windows. Vous devez utiliser la même version vérifiée de *la \_32.dllWs2* que la version commerciale qui a été utilisée sur le système en cours de test. Notez également que le comportement qui s’exécute sous une build vérifiée n’est pas le même que celui de l’exécution avec une version commerciale.

**Remarque**  Les SDK Windows pour Windows Server 2008 et versions ultérieures n’incluent plus les versions de débogage spéciales du *\_32.dllWs2*. Les développeurs doivent utiliser le suivi Winsock à l’aide d’ETW, car cette fonctionnalité ne nécessite pas de versions Debug.

## <a name="winsock-debug-and-trace-facility-on-windows-server-2003-and-windows-xp"></a>Fonctionnalité de débogage et de traçage Winsock sur Windows Server 2003 et Windows XP

Les versions antérieures de Windows antérieures à Windows 8 et Windows Server 2012 prennent en charge une fonctionnalité de débogage et de traçage primitive distincte qui est incluse comme un exemple avec les SDK Windows et l’ancien SDK de plateforme. La fonction de débogage/trace ne doit être utilisée que sur Windows Server 2003 et Windows XP où le suivi Winsock n’est pas pris en charge.

Si le SDK Windows pour Windows 7 est installé à l’emplacement par défaut, cette fonctionnalité de suivi Winsock primitive est installée dans le dossier suivant :

**C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ exemples \\ NetDs \\ Winsock \\ DT \_ dll**

Le fichier *DbgSpec.doc* dans ce dossier fournit une documentation sur cette fonctionnalité de trace primitive. L’exemple de code dans le \_ dossier de la dll DT doit être compilé pour utiliser cette fonctionnalité. Les développeurs sont libres d’utiliser le code source pour développer des versions de la DLL Debug/trace qui répondent à leurs besoins spécifiques.

Notez que cette fonctionnalité de trace Winsock primitive ne fonctionne que si la version de débogage de *Ws2 \_32.dll* installée. Vous devez donc obtenir une version vérifiée de la *\_32.dllWs2* qui correspond à la version de Windows et au Service Pack sur lequel vous effectuez le test.

Une limitation de cette fonctionnalité de \_ trace de dll DT primitive est que l’exemple de code utilise un verrou global (section critique) pour chaque appel de fonction Winsock. Cette fonctionnalité n’est donc pas utile dans le traitement des conditions de concurrence. L’exemple de code doit être largement réécrit pour rendre cette fonctionnalité de trace utile pour gérer la plupart des problèmes Winsock réels (en remplaçant les verrous globaux). Cet exemple de code permet aux développeurs de suivre les appels de procédure, les retours de procédure, les valeurs de paramètre et les valeurs de retour.

Les développeurs peuvent utiliser ce mécanisme primitif pour suivre les appels de procédure, les retours de procédure, les valeurs de paramètre et les valeurs de retour. Les valeurs de paramètre et les valeurs de retour peuvent être modifiées lors de l’appel de procédure ou du retour de procédure. Si vous le souhaitez, un appel de procédure peut être empêché ou redirigé. Avec un accès à ce niveau d’informations et de contrôle, un développeur est mieux en mesure d’isoler un problème dans l’application, le service *Ws2 \_32.dll* ou le fournisseur de services.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Suivi Winsock](winsock-tracing.md)
</dt> </dl>

 

 



