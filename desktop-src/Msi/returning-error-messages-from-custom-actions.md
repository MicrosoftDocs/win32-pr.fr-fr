---
description: Cette section explique comment envoyer des messages à partir d’actions personnalisées qui effectuent réellement une partie de l’installation en appelant une bibliothèque de liens dynamiques ou un script.
ms.assetid: 637efccf-920d-421d-9183-528cc3515bf8
title: Retour de messages d’erreur à partir d’actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c951b0e86d3120b989605572f15681582ac437fca5981852413331a3e63e684
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869119"
---
# <a name="returning-error-messages-from-custom-actions"></a>Retour de messages d’erreur à partir d’actions personnalisées

Cette section explique comment envoyer des messages à partir d’actions personnalisées qui effectuent réellement une partie de l’installation en appelant une bibliothèque de liens dynamiques ou un script. Notez que le [type d’action personnalisé 19](custom-action-type-19.md) envoie uniquement un message d’erreur spécifié, retourne un échec, puis met fin à l’installation. Le type d’action personnalisé 19 n’effectue aucune partie de l’installation.

Pour envoyer un message d’erreur à partir d’une action personnalisée qui utilise une [bibliothèque de liens dynamiques](dynamic-link-libraries.md) (dll), appelez l’action personnalisée [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage). Notez que les actions personnalisées lancées par une [action ControlEvent,](doaction-controlevent.md) peuvent envoyer des messages avec la méthode de [**message**](session-message.md) , mais ne peuvent pas envoyer de message avec **MsiProcessMessage**. sur les systèmes antérieurs à Windows Server 2003, les actions personnalisées lancées par une action controlevent, ne peuvent pas envoyer de messages avec **MsiProcessMessage** ou la méthode de **Message** . pour plus d’informations, consultez [envoi de Messages à Windows Installer à l’aide de MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).

**Pour afficher un message d’erreur à partir d’une action personnalisée à l’aide d’une DLL**

1.  L’action personnalisée doit appeler [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) et transmettre les paramètres *hInstall*, *eMessageType* et *hRecord*. Le descripteur de l’installation, [type d’action personnalisée 19](custom-action-type-19.md), peut être fourni à l’action personnalisée, comme décrit dans [accès à la session de programme d’installation actuelle à partir d’une action personnalisée](accessing-the-current-installer-session-from-inside-a-custom-action.md) ou de [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) ou [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea).
2.  Le paramètre *eMessageType* doit spécifier l’un des types de messages comme indiqué dans [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).
3.  Le paramètre *hRecord* de la fonction [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) dépend du type de message. consultez [envoi de Messages à Windows Installer à l’aide de MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md). Si le message contient des données mises en forme, entrez le message dans la table d' [Erreurs](error-table.md) en utilisant la mise en forme décrite dans [mise en forme](formatted.md).

Pour envoyer un message d’erreur à partir d’une action personnalisée qui utilise des [scripts](scripts.md), l’action personnalisée peut appeler la méthode de [**message**](session-message.md) de l’objet de [**session**](session-object.md) .

**Pour afficher un message d’erreur à partir d’une action personnalisée à l’aide d’un script**

1.  L’action personnalisée doit appeler la méthode de [**message**](session-message.md) de l’objet de [**session**](session-object.md) et transmettre les paramètres *Kind* et *Record*.
2.  Le *genre* de paramètre doit spécifier l’un des types de messages listés dans la méthode de [**message**](session-message.md) .
3.  Le paramètre d' *enregistrement* de la méthode de [**message**](session-message.md) dépend du type de message. Si le message contient des données mises en forme, entrez le message dans la table d' [Erreurs](error-table.md) en utilisant la mise en forme décrite dans [mise en forme](formatted.md).

Les actions personnalisées utilisant des [fichiers exécutables](executable-files.md) ne peuvent pas envoyer de message en appelant [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) ou la méthode [**message**](session-message.md) , car ils ne peuvent pas obtenir de handle pour l’installation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Valeurs de retour de l’action personnalisée](custom-action-return-values.md)
</dt> </dl>

 

 



