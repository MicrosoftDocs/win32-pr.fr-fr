---
description: le SDK Windows contient des exemples de code et des outils utiles pour vous aider à comprendre et à utiliser le capteur Windows et la plateforme d’emplacement, ainsi que les api associées.
ms.assetid: e31174f6-1c2b-4d97-b6b6-e54825ff47f5
title: À propos des exemples et des outils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6126ec5e07829cfd17c2b07313bb104140c6fee6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013560"
---
# <a name="about-the-samples-and-tools"></a>À propos des exemples et des outils

le SDK Windows contient des exemples de code et des outils utiles pour vous aider à comprendre et à utiliser le capteur Windows et la plateforme d’emplacement, ainsi que les api associées.

## <a name="samples"></a>Exemples

le SDK Windows comprend les exemples d’API de capteur suivants. vous trouverez les exemples d’API de capteur dans le dossier nommé \\ samples \\ winui \\ sensors, où vous avez installé le SDK Windows. par exemple, si vous avez installé le SDK Windows sur le lecteur C, vous trouverez les exemples dans le dossier suivant : C : \\ Program Files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ winui \\ sensors.



| Nom d’exemple       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AmbientLightAware | Cet exemple MFC montre comment utiliser l’API de capteur en lisant les données des capteurs de lumière ambiante sur l’ordinateur et en modifiant la taille du texte en fonction des conditions d’éclairage. Vous pouvez voir le code qui montre comment gérer des événements et comment demander des autorisations utilisateur. Vous pouvez également voir un exemple de gestion de l’interface utilisateur en fonction de différentes conditions d’éclairage. Pour plus d’informations, consultez [création d' Light-Aware interfaces utilisateur](creating-light-aware-user-interfaces.md).<br/> Visual Studio 2008 doit être installé pour générer cet exemple.<br/> |



 

Pour plus d’informations, consultez le fichier nommé ReadMe.txt inclus avec l’exemple.

Vous pouvez également télécharger l’exemple AmbientLightAware à partir de la Galerie de code. Pour plus d’informations, consultez la page de téléchargement de la prise en charge de la [lumière ambiante](/samples/browse/?redirectedfrom=MSDN-samples) .

## <a name="tools"></a>Outils

le SDK Windows comprend un capteur de lumière virtuelle que vous pouvez utiliser pour simuler un appareil de capteur de lumière matériel. Vous pouvez utiliser cet outil pour fournir des données à l’exemple AmbientLightAware pour voir comment le code de l’exemple fonctionne.

Le tableau suivant décrit les fichiers que vous devez utiliser pour exécuter le capteur de lumière virtuelle. ces fichiers se trouvent dans le dossier nommé Bin, dans lequel vous avez installé le SDK Windows. par exemple, si vous avez installé le SDK Windows sur le lecteur C sur un ordinateur 32 bits, vous trouverez les fichiers de capteur de lumière virtuelle dans le dossier suivant : C : \\ Program files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ Bin. Sur les ordinateurs 64 bits, vous devez utiliser la version 64 bits de l’outil. dans le SDK Windows, les outils 64 bits se trouvent dans le sous-dossier nommé x64.



| Nom de fichier                    | Description                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| VirtualLightSensor.exe       | Ce programme fournit un contrôle Slider qui vous permet de modifier le niveau des données de lumière que le capteur virtuel signale. |
| VirtualLightSensorDriver.dll | Pilote de capteur logique qui simule un capteur de lumière.                                                                       |
| VirtualLightSensorDriver. inf | Fichier INF du pilote de capteur de lumière virtuelle.                                                                              |



 

### <a name="installing-the-virtual-light-sensor"></a>Installation du capteur de lumière virtuelle

Avant d’utiliser l’application de capteur d’éclairage virtuel, vous devez installer le pilote de capteur logique. Suivez ces étapes :

1.  Ouvrez une fenêtre de commande en tant qu’administrateur.
2.  accédez au dossier SDK Windows Bin.
3.  Tapez **PnPUtil-a VirtualLightSensorDriver. inf**.
4.  Quand vous y êtes invité, cliquez sur **installer ce pilote logiciel quand même**.
5.  Attendez que la fenêtre de commande signale que le pilote a été correctement installé.

### <a name="running-the-virtual-light-sensor"></a>Exécution du capteur de lumière virtuelle

Pour exécuter le capteur de lumière virtuelle, il vous suffit de double-cliquer sur le fichier .exe. Veillez à activer le capteur quand vous y êtes invité.

Lorsque vous exécutez le programme, vous pouvez remarquer qu’il y a un délai avant que le capteur ne soit disponible. L’interface utilisateur du capteur de lumière virtuelle affiche le message « en attente » dans la barre de titre, tandis que le gestionnaire de capteurs logiques crée un nœud de périphérique pour le capteur logique. Une fois le message en attente supprimé, vous pouvez utiliser le curseur pour définir le niveau de sortie Lux pour le capteur de lumière virtuelle.

L’illustration suivante montre l’interface utilisateur du capteur d’éclairage virtuel dans son état prêt.

![interface utilisateur du capteur d’éclairage virtuel](images/virtuallightsensor.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des capteurs logiques](about-logical-sensors.md)
</dt> <dt>

[**catégorie de capteur \_ \_ Light**](sensor-category-light.md)
</dt> </dl>

 

