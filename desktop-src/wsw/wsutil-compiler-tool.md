---
title: Outil compilateur WsUtil
description: l’outil Windows compilateur de Services Web, WsUtil.exe, prend en charge le modèle de service et la sérialisation des types de données. Il traite les documents WSDL, de schéma et de stratégie XML et génère des en-têtes et des fichiers sources C.
ms.assetid: 7fc3f1bd-ead2-4095-9592-d2ad88d56e7a
keywords:
- Services Web de l’outil compilateur WsUtil pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa83da50888fcf2d66fac7fb00b3a31ae2919738
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234348"
---
# <a name="wsutil-compiler-tool"></a>Outil compilateur WsUtil

l’outil Windows compilateur de Services Web, WsUtil.exe, prend en charge le [modèle de service](service-model-layer-overview.md) et la [sérialisation](serialization.md) des types de données. Il traite les documents WSDL, de schéma et de stratégie XML et génère des en-têtes et des fichiers sources C. Cet outil est similaire à l’outil compilateur WSDL pour le code managé, mais il est destiné au code natif à la place.

Pour prendre en charge le [modèle de service](service-model-layer-overview.md), WsUtil.exe génère des en-têtes à utiliser à la fois pour le client et le service. Il génère un fichier proxy C pour le côté client et des fichiers stub C pour le côté service, si nécessaire.

Pour prendre en charge la [sérialisation](serialization.md), le compilateur génère des en-têtes pour les descriptions d’éléments pour les définitions d’éléments globaux et toutes les informations de définition de type dans les fichiers de proxy qui sont consommés par le moteur de sérialisation.


Pour obtenir des options de ligne de commande pour le traitement des fichiers WSDL, des fichiers de schéma XML et des fichiers de stratégie de service Web, consultez les rubriques suivantes :

-   [Outil du compilateur de service Web](web-service-compiler-tool.md)
-   [WSDL et contrats de service](wsdl-support.md)
-   [Prise en charge des schémas](schema-support.md)
-   [Prise en charge des stratégies](policy-support.md)

## <a name="security"></a>Sécurité

Lorsque vous utilisez WsUtil, tenez compte des points suivants et observez les précautions appropriées :

-   Wsutil ne récupère pas les métadonnées XML sur le réseau et Wsutil ne résout pas les instructions import et/ou include dans les fichiers de métadonnées d’entrée. Wsutil ouvre et lit les fichiers WSDL, XSD et de stratégie. Les métadonnées XML ne sont pas résistantes aux falsifications. Veillez à utiliser uniquement WSDL, XSD et les fichiers de stratégie sont acquis à partir de la source approuvée et veillez à protéger les fichiers contre toute falsification avant et après les avoir utilisés. Examinez attentivement le contenu des fichiers d’entrée et vérifiez que le contenu des fichiers est sécurisé pour une utilisation dans l’application. Wsutil.exe n’effectue aucune vérification de l’authenticité des fichiers de métadonnées.
-   Wsutil génère des fichiers d’en-tête et stub, qui ne sont pas résistants aux falsifications. Vous devez définir les droits d’accès au niveau corrects sur les fichiers sources générés par wsutil.exe pour empêcher l’accès unauthoritized à ces fichiers. Wsutil utilise System. IO. StreamWriter pour créer les fichiers de sortie.
-   Les utilisateurs doivent savoir que Wsutil peut remplacer leurs fichiers locaux et qu’ils doivent veiller à spécifier des noms de fichiers sûrs et des répertoires pour les fichiers de sortie à l’aide du commutateur/out.
-   Wsutil ou wsutilhelper.dll chargées dans wsutil.exe peut s’arrêter de manière inattendue ou consommer une grande quantité de ressources système lors d’une attaque ou lors du traitement d’une très grande quantité de métadonnées d’entrée. L’outil est conçu pour être utilisé au moment du développement uniquement. cet outil ne doit être utilisé qu’en tant qu’outil de développement. Il se peut qu’il ne soit pas possible de l’utiliser dans la couche intermédiaire pour traiter les informations de stratégie.
-   Wsutilhelper.dll DLL d’assistance est chargée dans les wsutil.exe managées pour traiter les informations de stratégie. L’utilisateur doit s’assurer qu’aucun fichier binaire malveillant portant le même nom de fichier n’existe dans le chemin d’accès binaire. De même, l’utilisateur doit s’assurer que dans l’environnement de génération, le chemin d’accès binaire est correctement configuré et qu’il n’existe aucun fichier binaire malveillant portant le même nom de « wsutil.exe ».
-   Wsutil génère une annotation SAL pour les opérations et les champs de structure lorsque cela est possible. L’utilisateur des fichiers générés par Wsutil doit respecter les exigences spécifiées par le biais de l’annotation SAL.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble de la couche de modèle de service](service-model-layer-overview.md)
</dt> <dt>

[Sérialisation](serialization.md)
</dt> <dt>

[Outil du compilateur de service Web](web-service-compiler-tool.md)
</dt> <dt>

[Prise en charge WSDL](wsdl-support.md)
</dt> <dt>

[Prise en charge des schémas](schema-support.md)
</dt> <dt>

[Prise en charge des stratégies](policy-support.md)
</dt> </dl>

 

 




