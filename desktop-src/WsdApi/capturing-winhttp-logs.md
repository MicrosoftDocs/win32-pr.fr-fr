---
description: Les journaux WinHTTP peuvent être utilisés pour aider à résoudre les problèmes liés aux applications WSDAPI. Cela est utile lorsque l’échange de métadonnées échoue ou lorsque la négociation SSL/TLS échoue.
ms.assetid: 75ba330d-afcd-4d8f-93c7-a1b9f80dd050
title: Capture des journaux WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378801e97b2eef8c1ea0c40a5973844d75a94e02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115027"
---
# <a name="capturing-winhttp-logs"></a>Capture des journaux WinHTTP

Les journaux [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) peuvent être utilisés pour aider à résoudre les problèmes liés aux applications wsdapi. Cela est utile lorsque l’échange de métadonnées échoue ou lorsque la négociation SSL/TLS échoue.

Cette procédure montre comment capturer des journaux WinHTTP sur le PC client. L’application cliente WSDAPI ne doit pas être en cours d’exécution lorsque la journalisation est activée. Si l’application cliente est en cours d’exécution lorsque la journalisation est activée, le client et/ou le PC doivent être redémarrés pour que les WS-Discovery et le trafic d’échange de métadonnées s’affichent dans les journaux WinHTTP.

**Pour capturer les journaux WinHTTP**

1.  Ouvrez une fenêtre d’invite de commandes avec élévation de privilèges sur le PC client.
2.  Exécutez la commande suivante : **netsh WinHTTP Set Tracing trace-file-prefix = "C : \\ temp \\ DPWS" niveau = verbose format = ANSI State = Enabled Max-trace-file-Size = 1073741824**

    Cette commande active la journalisation WinHTTP. Tous les fichiers journaux sont stockés dans le répertoire C : \\ temp, et les noms de fichiers commencent par le préfixe DPWS. Au plus 1 Go de fichiers journaux seront stockés.

3.  Si le processus utilisant WinHTTP sur le client est déjà en cours d’exécution, redémarrez l’ordinateur. Par exemple, si les API de [détection de fonction](/previous-versions/windows/desktop/fundisc/fd-portal) sont utilisées, l’ordinateur doit être redémarré. Les API de détection de fonction appellent WinHTTP depuis l’intérieur d’un hôte de service, qui a peut-être déjà démarré lorsque le suivi a été activé.
4.  Démarrez l’application cliente WSDAPI. L’application en cours de débogage ou le client de débogage WSD peut être utilisé.
5.  Reproduire l’échec de l’application.
6.  Arrêtez l’application cliente basée sur WSDAPI.
7.  Si le processus qui utilise WinHTTP n’est pas terminé avec l’application cliente, redémarrez l’ordinateur. Par exemple, si les API de [détection de fonction](/previous-versions/windows/desktop/fundisc/fd-portal) sont utilisées, l’ordinateur doit être redémarré.
8.  Exécutez la commande suivante : **netsh WinHTTP Set Tracing State = Disabled**

    Cette commande désactive la journalisation WinHTTP.

9.  Inspectez les journaux DPWS dans C : \\ temp et vérifiez que les demandes et les messages requis ont été envoyés.
10. Si la communication de canal sécurisé (HTTPs) est utilisée, vérifiez les défaillances SSL/TLS.

Une fois les journaux WinHTTP capturés, les journaux peuvent être examinés pour rechercher la cause d’un échec d’application WSDAPI. Notez que l’éditeur de texte utilisé pour afficher ces journaux doit être exécuté en tant qu’administrateur. Pour plus d’informations, consultez [utilisation de la journalisation WinHTTP pour vérifier obtenir le trafic](using-winhttp-logging-to-verify-get-traffic.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[Utilisation de la journalisation WinHTTP pour vérifier la récupération du trafic](using-winhttp-logging-to-verify-get-traffic.md)
</dt>
</dl>
