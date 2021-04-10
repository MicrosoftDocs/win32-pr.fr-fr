---
description: Commandes
ms.assetid: f579745a-5327-4c8b-bfa7-fe81d9657a3b
title: Commandes (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974c6b2b68949e53ae778ed56adcfcb10d2edd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201380"
---
# <a name="commands-wpd-api"></a>Commandes (API WPD)

L’application cliente et le pilote communiquent à l’aide de commandes envoyées à partir du client (via l’API Windows Mobile Device) au pilote (via l’infrastructure de pilote User-Mode). Une commande peut ou non inclure un paramètre et peut ou non retourner un résultat. Un client peut envoyer une commande de manière explicite, en appelant la méthode [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) ou la méthode **IPortableDeviceService : SendCommand** , ou implicitement, en appelant l’une des méthodes des interfaces clientes. Certaines commandes peuvent être envoyées uniquement de manière explicite ; celles-ci sont indiquées dans la documentation de la commande. Les pages de référence de commande décrivent l’objectif d’une commande, ainsi que les paramètres qu’elle s’attend à recevoir et les paramètres qu’elle doit retourner.

Une commande est identifiée par une structure **PROPERTYKEY** . Il se compose de deux parties : une partie GUID (le membre *fmtid* ) et une partie DWORD (le membre *PID* ). La partie GUID est utilisée pour indiquer la catégorie à laquelle la commande appartient (les commandes associées appartiennent à la même catégorie et, par conséquent, ont le même *fmtid*). La partie DWORD indique l’ID de commande et est utilisée pour distinguer les commandes individuelles au sein d’une catégorie de commande (les valeurs *PID* pour les commandes dans la même catégorie sont différentes).

Le tableau suivant répertorie les catégories de commandes que les appareils mobiles Windows définit. Les fabricants de périphériques peuvent définir leurs propres commandes en créant leurs propres catégories de commandes et ID de commande. Toutefois, un fabricant ne doit pas ajouter de commandes aux catégories répertoriées ci-dessous, car celles-ci sont réservées par Microsoft.

**Catégories de commandes**



| Catégorie de commande                         | Description                                                                                                                             |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **WPD, \_ catégorie \_ commune**                | Les commandes qui sont communes à tous les objets et périphériques.                                                                                    |
| **indicateurs d’appareil de la \_ catégorie wpd \_ \_**         | Commandes utilisées pour récupérer des informations facultatives sur l’appareil qui peuvent être utilisées pour améliorer l’expérience de l’utilisateur final.                         |
| **\_SMS de catégorie wpd \_**                   | Commandes utilisées pour les appareils qui prennent en charge la fonctionnalité SMS (Short Message Service), qui est généralement exposée sur les téléphones portables. |
| **\_capture d' \_ \_ image continue de catégorie \_ wpd** | Commandes utilisées pour les appareils qui prennent en charge la capture d’images continues.                                                                    |
| **\_stockage de catégorie wpd \_**               | Commandes utilisées pour le stockage des objets fonctionnels.                                                                                  |



 

Les commandes spécifiques définies pour chacun de ces types sont présentées dans les tableaux suivants, organisés par type de commande.

**Catégorie \_ commune de la catégorie wpd \_**



| Commande                                                                                | Description        |
|----------------------------------------------------------------------------------------|--------------------|
| [**\_appareil de \_ \_ réinitialisation commune de commande wpd \_**](wpd-command-common-reset-device-command.md) | Réinitialise l’appareil. |



 

**\_Catégorie d' \_ indicateurs d’appareil de catégorie wpd \_**



| Commande                                                                                                              | Description                                                                      |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**\_options d’appareil de commande wpd obtient l' \_ \_ \_ \_ emplacement du contenu \_**](wpd-command-device-hints-get-content-location-command.md) | Récupère les ID d’objet des dossiers qui peuvent contenir un objet d’un type spécifié. |



 

**Catégorie de stockage de \_ catégorie wpd \_**



| Commande                                                                     | Description                                                         |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**\_éjection de \_ stockage de commande wpd \_**](wpd-command-storage-eject-command.md)   | Éjecte un support de stockage qui peut être éjecté à distance par le pilote. |
| [**\_format de \_ stockage des commandes wpd \_**](wpd-command-storage-format-command.md) | Met en forme un objet fonctionnel de stockage sur l’appareil.                  |



 

**Catégorie des \_ SMS de catégorie wpd \_**



| Commande                                                         | Description                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| [**\_commande wpd \_ SMS \_ Send**](wpd-command-sms-send-command.md) | Lance l’envoi d’un message SMS par un objet fonctionnel SMS. |



 

**\_Catégorie de \_ \_ capture d’image continue de catégorie wpd \_**



| Commande                                                                                                   | Description                                                         |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**démarrage de la \_ \_ \_ capture d’image continue \_ de la commande wpd \_**](wpd-command-still-image-capture-initiate-command.md) | Lance une capture d’image continue par un objet fonctionnel d’image continue. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de référence de programmation**](programming-reference.md)
</dt> </dl>

 

 



