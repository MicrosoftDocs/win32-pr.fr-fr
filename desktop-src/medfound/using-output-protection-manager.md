---
description: 'En savoir plus sur : utilisation de Output Protection Manager'
ms.assetid: 01edc17e-e71c-4772-a03c-09c9a2b8400f
title: Utilisation de Output Protection Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bf4def3b0575dd706ae5f0c62924b6f1375a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521500"
---
# <a name="using-output-protection-manager"></a>Utilisation de Output Protection Manager

Cette rubrique explique comment utiliser le gestionnaire de protection de sortie (OPM) pour protéger le contenu vidéo lorsqu’il transite par un connecteur physique sur un périphérique d’affichage. Cette rubrique contient les sections suivantes :

-   [Sorties vidéo](#video-outputs)
-   [Initialisation d’une session OPM](#initializing-an-opm-session)
-   [Envoi de demandes d’État OPM](#sending-opm-status-requests)
-   [Envoi de commandes OPM](#sending-opm-commands)
-   [Gestion d’une sortie vidéo désactivée](#sending-opm-commands)
-   [Utilisation de HDCP pour protéger du contenu](#using-hdcp-to-protect-content)

Le contenu vidéo Premium est généralement chiffré pour le protéger contre la duplication non autorisée. Bien entendu, la vidéo doit être déchiffrée avant d’être affichée. Les frames décompressés et non compressés doivent ensuite circuler sur le périphérique d’affichage à travers un connecteur physique. Les fournisseurs de contenu peuvent exiger que les images vidéo soient protégées à ce stade, lors de leur déplacement sur le connecteur physique.

Il existe différents mécanismes de protection à cet effet, notamment High-Bandwidth Digital protection du contenu (HDCP) et DisplayPort protection du contenu (DPCP) pour les sorties numériques ; et le système de gestion de la génération de copie-analogique (CGMS-A) pour les sorties analogiques. En règle générale, ces mécanismes impliquent le chiffrement ou le brouillage du signal avant qu’il ne passe à l’écran.

OPM permet à une application d’appliquer des mécanismes de protection de contenu sur la sortie vidéo. À l’aide de OPM, l’application envoie des commandes et des demandes d’État au pilote Graphics via un canal sécurisé sécurisé. OPM permet à une application d’effectuer les opérations suivantes :

-   Vérifiez qu’un pilote graphique a été signé par Microsoft.
-   Configurez un canal de communication approuvé avec le pilote.
-   Appliquer des mécanismes de protection du contenu sur la sortie physique.

OPM remplace la protection de sortie certifiée Protcol (COPP) et utilise une API similaire. Pour des raisons de compatibilité descendante, l’interface OPM peut émuler l’interface COPP. Les différences entre OPM et COPP sont les suivantes :

-   OPM utilise des certificats X. 509, tandis que COPP utilise un format de certificat propriétaire.
-   OPM prend en charge les répéteurs HDCP.
-   Les applications qui utilisent OPM n’ont pas besoin d’analyser les messages de renouvellement du système HDCP (SRMs).
-   OPM peut être utilisé lorsque l’affichage graphique utilise le mode de clonage. COPP ne prend pas en charge le mode clone.

Si votre application utilise le chemin d’accès de média protégé (PMP) pour lire le contenu vidéo, vous n’avez pas besoin d’utiliser l’API OPM, car l’PMP effectue tous les appels OPM requis. L’API OPM est disponible pour les applications qui n’utilisent pas le PMP.

OPM est disponible dans Windows Vista et versions ultérieures, mais l’API n’a pas été rendue publique jusqu’à Windows 7. Pour utiliser OPM dans une application, vous devez disposer des en-têtes et des fichiers de bibliothèque du kit de développement logiciel (SDK) Windows 7. Vous n’avez pas besoin de redistribuer des dll pour utiliser OPM dans Windows Vista ou Windows Server 2008.

## <a name="video-outputs"></a>Sorties vidéo

Une carte graphique peut avoir plusieurs sorties physiques, chacune avec ses propres fonctionnalités. Avant qu’une application ne lise du contenu protégé, elle doit définir les mécanismes de protection appropriés sur chaque sortie vidéo associée à la carte graphique qui affichera la vidéo. Les mécanismes de protection à appliquer dépendent des règles d’utilisation du contenu.

Chaque sortie vidéo est représentée par une instance de l’interface [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) . Vous pouvez utiliser un périphérique Direct3D ou surveiller les descripteurs pour obtenir les sorties vidéo.

Utilisation d’un appareil Direct3D :

1.  Récupérez le pointeur **IDirect3DDevice9** pour le périphérique Direct3D que votre application utilisera pour créer des surfaces qui contiendront les images vidéo.
2.  Appelez la fonction [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) . Cette fonction alloue un tableau de pointeurs [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) , un pour chaque sortie.

Utilisation des handles de moniteur :

1.  Appelez **EnumDisplayMonitors** pour récupérer les handles **HMONITOR** qui correspondent à la fenêtre vidéo. Plusieurs analyses peuvent être associées à la même fenêtre, de sorte que vous pouvez recevoir plusieurs descripteurs **HMONITOR** .
2.  Pour chaque handle d’analyse, appelez [**OPMGetVideoOutputsFromHMONITOR**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor). Cette fonction alloue un tableau de pointeurs [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) , un pour chaque sortie.

## <a name="initializing-an-opm-session"></a>Initialisation d’une session OPM

Avant d’envoyer des commandes ou des demandes d’État OPM, l’application doit vérifier que la sortie vidéo est approuvée et établir une clé de session. La clé de session est utilisée pour signer les données échangées entre l’application et le pilote Graphics.

L’API OPM définit une liaison qui établit l’approbation et définit la clé de session. Vous devez effectuer cette négociation pour chaque instance de l’interface [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) , comme suit :

1.  Appelez [**IOPMVideoOutput :: StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization). Cette méthode récupère deux éléments de données :
    -   Nombre aléatoire, généré par le pilote. Vous allez utiliser ce numéro pour terminer la négociation.
    -   Chaîne de certificats X. 509 du pilote.
2.  Vérifiez que la chaîne de certificats a été signée par Microsoft.
    > [!Note]  
    > La révocation de certificat est en dehors de la portée de OPM.

     

3.  Récupérez la clé publique du pilote à partir de la chaîne de certificats.
4.  Générez une clé de session AES 128 bits.
5.  Générez deux nombres aléatoires de 32 bits :

    -   Numéro de séquence de départ pour les demandes d’État OPM.
    -   Numéro de séquence de départ pour les commandes OPM.

    Ces valeurs doivent être générées à l’aide d’un générateur de nombres pseudo-aléatoires sécurisé par chiffrement, tel que **CryptGenRandom**.

6.  Copiez le nombre aléatoire du pilote (obtenu à l’étape 1), la clé de session et les deux numéros séquentiels dans une structure de [**\_ \_ \_ paramètres d’initialisation chiffrée opm**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters) , comme décrit dans [**IOPMVideoOutput :: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization).
7.  Chiffrez la structure des [**\_ \_ \_ paramètres d’initialisation chiffrée OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters) avec RSAES-OAEP, à l’aide de la clé publique du pilote, qui se trouve dans le certificat du pilote.
8.  Appelez [**IOPMVideoOutput :: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization).

## <a name="sending-opm-status-requests"></a>Envoi de demandes d’État OPM

Les demandes d’État OPM renvoient des informations sur la sortie vidéo, telles que le type de connecteur physique et le niveau de protection actuel. Pour obtenir la liste des types de demande, consultez [demandes d’État OPM](opm-status-requests.md).

Pour envoyer une demande d’État, procédez comme suit.

1.  Initialisez une structure de [**\_ paramètres d’extraction d' \_ informations \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) comme indiqué dans le tableau suivant.

    | Membre               | Description                                                                                                                                                                                                                                                                                                                                                                 |
    |----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **omac**             | Ignorez ce champ pour l’instant.                                                                                                                                                                                                                                                                                                                                                    |
    | **rnRandomNumber**   | Nombre aléatoire 128 bits sécurisé par chiffrement. Chaque fois que vous faites une demande d’État, générez toujours un nouveau nombre aléatoire, même si vous effectuez la même requête. Stockez le nombre dans une variable, car vous devrez y faire référence ultérieurement.                                                                                                                             |
    | **guidInformation**  | GUID qui identifie la demande d’État. Pour obtenir la liste des demandes d’État, consultez [demandes d’État OPM](opm-status-requests.md).                                                                                                                                                                                                                                               |
    | **ulSequenceNumber** | Numéro séquentiel. Pour la première demande d’État, utilisez le numéro de séquence de départ que vous avez spécifié dans la méthode [**IOPMVideoOutput :: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) (étape 5 de l' [initialisation d’une session OPM](#initializing-an-opm-session)). Chaque fois que vous effectuez une autre demande d’État, incrémentez ce nombre de 1. |
    | **abParameters**     | Tableau d’octets qui contient des données d’entrée supplémentaires pour la demande. Le format des données d’entrée est indiqué dans la rubrique de référence pour chaque demande d’État.                                                                                                                                                                                                                    |
    | **cbParametersSize** | Taille des données valides dans le tableau **abParameters** . Le contenu du reste du tableau n’est pas défini.                                                                                                                                                                                                                                                              |

    

     

2.  Calculez l’OMAC CBC MAC (-1) pour calculer un hachage pour le bloc de données qui apparaît après le membre **OMAC** , puis affectez la valeur au membre **OMAC** . Consultez l' [exemple de code OPM](opm-example-code.md).
3.  Appelez la méthode [**IOPMVideoOutput :: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) . Transmettez un pointeur vers la structure des paramètres de l' [**\_ obtenir des \_ informations \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) et un pointeur vers une structure d' [**\_ \_ informations OPM demandée**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) . La réponse du pilote est écrite dans la structure d' **\_ \_ informations demandée par OPM** .
    -   Le membre **OMAC** de cette structure contient un OMAC calculé pour les données qui suivent ce membre.
    -   Le membre **abRequestedInformation** est un tableau d’octets qui contient les données de sortie de la réponse. Le format des données de sortie est indiqué dans la rubrique de référence pour chaque demande d’État.
4.  Calculez un OMAC pour la structure d’informations de l' [**OPM \_ \_ demandée**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) , à l’exclusion du membre **OMAC** . Vérifiez que OMAC correspond à la valeur du membre **OMAC** .
5.  Assurez-vous que le membre **cbRequestedInformationSize** de la structure d' [**\_ \_ informations demandée par OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) donne la taille appropriée pour les données de sortie. Par exemple, les données de sortie de la requête de [**\_ \_ \_ type de connecteur OPM obtenir**](opm-get-connector-type.md) sont une structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) , donc la valeur de **cbRequestedInformationSize** doit être `sizeof(OPM_STANDARD_INFORMATION)` .
6.  Effectuez un cast du membre **abRequestedInformation** de la structure d’informations de la [**\_ demande \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) vers la structure de données de sortie correcte. Par exemple, si la demande d’état [**est \_ \_ \_ type de connecteur OPM obtenir**](opm-get-connector-type.md), effectuez un cast de **AbRequestedInformation** en structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .
7.  Assurez-vous que le membre **rnRandomNumber** de la structure de données de sortie correspond à la valeur de **rnRandomNumber** de l’étape 1.
8.  Vérifiez le membre **ulStatusFlags** de la structure des données de sortie, comme décrit dans [gestion d’une sortie vidéo désactivée](#handling-a-disabled-video-output).

Si l’une des vérifications des étapes 5 à 8 échoue, l’application doit cesser d’indiquer le contenu protégé.

## <a name="sending-opm-commands"></a>Envoi de commandes OPM

Les commandes OPM sont utilisées pour définir le niveau de protection et d’autres paramètres sur la sortie vidéo. L’envoi d’une commande OPM est semblable à l’envoi d’une demande d’État, à ceci près qu’il n’y a pas de données de réponse du pilote. Pour obtenir la liste des commandes, consultez les [commandes OPM](opm-commands.md).

Pour envoyer une commande OPM, procédez comme suit.

1.  Remplissez une structure [**de \_ \_ paramètres OPM configure**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) comme indiqué dans le tableau suivant.

    | Membre                | Description                                                                                                                                                                                                                                                                                                                                                   |
    |-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **omac**              | Ignorez ce champ pour l’instant.                                                                                                                                                                                                                                                                                                                                      |
    | **guidSetting**       | GUID qui identifie la commande. Pour obtenir la liste des commandes, consultez les [commandes OPM](opm-commands.md).                                                                                                                                                                                                                                                             |
    | **ulSequenceNumber**  | Numéro séquentiel. Pour la première commande, utilisez le numéro de séquence de départ que vous avez spécifié dans la méthode [**IOPMVideoOutput :: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) (étape 5 de [l’initialisation d’une session OPM](#initializing-an-opm-session)). Chaque fois que vous envoyez une autre commande, incrémentez ce nombre de 1. |
    | **abParameters**      | Tableau d’octets qui contient des données d’entrée supplémentaires pour la commande. Le format des données d’entrée est indiqué dans la rubrique de référence pour chaque commande.                                                                                                                                                                                                             |
    | **cbSettingDataSize** | Taille des données valides dans le tableau **abParameters** . Le contenu du reste du tableau n’est pas défini.                                                                                                                                                                                                                                                |

    

     

2.  Calculez un OMAC pour le bloc de données qui apparaît après le membre **OMAC** , puis définissez cette valeur pour le membre **OMAC** .
3.  Appelez [**IOPMVideoOutput :: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).

Pour la plupart des commandes, il existe une demande d’État correspondante qui retourne l’état de la commande. Par exemple, la commande [**OPM \_ Set \_ protection \_ Level**](opm-set-protection-level.md) définit le niveau de protection et la commande [**OPM obtenir le \_ \_ \_ \_ niveau**](opm-get-virtual-protection-level.md) de protection virtuel obtient le niveau de protection actuel.

## <a name="handling-a-disabled-video-output"></a>Gestion d’une sortie vidéo désactivée

Une sortie vidéo peut se désactiver à tout moment pour empêcher l’utilisation non autorisée du contenu vidéo. Cela peut se produire si un mécanisme de protection ne fonctionne pas, car le pilote détecte une falsification, ou l’affichage a été déconnecté du connecteur physique. Lorsqu’une sortie vidéo est désactivée, aucune image vidéo n’est affichée.

Bien que la protection du contenu soit activée, une application doit régulièrement (au moins une fois toutes les 2 secondes) effectuer les étapes suivantes.

1.  Appelez [**IOPMVideoOutput :: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) pour envoyer au [**niveau de \_ protection OPM obtenir le \_ \_ \_ niveau de protection réel**](opm-get-actual-protection-level.md) ou [**OPM obtenir le \_ \_ \_ \_ niveau de protection virtuel**](opm-get-virtual-protection-level.md) . Les données de retour pour les deux commandes sont une structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .
2.  Vérifiez le membre **ulInformation** de la structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . Ce membre contient un indicateur qui indique si la protection du contenu est toujours activée. Si la protection du contenu est désactivée, arrêtez la vidéo immédiatement.
3.  Si la protection du contenu est activée, vérifiez le membre **ulStatusFlags** de la structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . Si aucun indicateur n’est défini, la sortie vidéo fonctionne correctement. Dans le cas contraire, la sortie vidéo est désactivée.

Les indicateurs suivants sont définis pour **ulStatusFlags**.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Indicateur</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>OPM_STATUS_LINK_LOST</strong></td>
<td>La protection de sortie a cessé de fonctionner pour une raison quelconque. par exemple, le périphérique d’affichage peut être débranché du conntector. Arrêtez la lecture et désactivez tous les mécanismes de protection de sortie.</td>
</tr>
<tr class="even">
<td><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></td>
<td>L’application doit rétablir la session OPM. Répondez comme suit :
<ol>
<li>Arrêter la lecture.</li>
<li>Désactivez tous les mécanismes de protection.</li>
<li>Libérer l’interface <a href="/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput"><strong>IOPMVideoOutput</strong></a> .</li>
<li>Recréez toutes les surfaces vidéo.</li>
<li>Créez un nouvel objet OPM et tentez de rétablir la protection du contenu. En cas d’échec, affiche un message d’erreur à l’utilisateur. Ne lisez plus de contenu vidéo.</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></td>
<td>Cet indicateur s’applique uniquement lorsque HDCP est utilisé et indique la présence d’un appareil HDCP révoqué. Arrêtez la lecture et désactivez tous les mécanismes de protection sur cette sortie vidéo. Lorsque cet indicateur est défini, l’indicateur <strong>OPM_STATUS_LINK_LOST</strong> est également défini.</td>
</tr>
<tr class="even">
<td><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></td>
<td>Le pilote a détecté une falsification. Arrêter la lecture et ne pas lire d’autres vidéos à l’aide de cette sortie vidéo. Il est également judicieux de cesser d’utiliser d’autres sorties vidéo, car le système risque d’être compromis.</td>
</tr>
</tbody>
</table>



 

## <a name="using-hdcp-to-protect-content"></a>Utilisation de HDCP pour protéger du contenu

Cette section décrit comment activer la protection de sortie HDCP à l’aide de OPM. Voici un aperçu général des étapes que l’application doit effectuer. Les détails sont fournis plus loin dans cette section.

1.  L’application devra peut-être fournir un SRM à la sortie vidéo. Le mécanisme de réception des SRMs est en dehors de l’étendue de l’interface OPM. Par exemple, SRMs peut être fourni dans le cadre d’un flux de diffusion.
2.  L’application active la protection de sortie HDCP.
3.  L’application lit le contenu vidéo. Périodiquement, l’application interroge le pilote pour s’assurer que HDCP est activé.
4.  Une fois la lecture terminée, l’application désactive HDCP.

### <a name="setting-the-srm"></a>Configuration de SRM

Pour définir le SRM, procédez comme suit.

1.  Initialisez une structure de [**\_ \_ \_ \_ paramètres SRM Set HDCP**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) avec le numéro de version SRM.
2.  Stockez le SRM dans une variable.
3.  Envoie une commande [**OPM \_ Set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) à la sortie vidéo. Utilisez la procédure décrite dans la rubrique [envoi de commandes OPM](#sending-opm-commands).
    -   Le membre **abParameters** de la structure des [**\_ \_ paramètres de configuration de opm**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) contient la structure des [**\_ \_ \_ \_ paramètres OPM Set HDCP**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) .
    -   Le paramètre *pbAdditionalParameters* de la méthode [**IOPMVideoOutput :: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) pointe vers la variable qui contient le SRM.
4.  Envoyer une demande d’état de la [**\_ \_ \_ \_ \_ version HDCP SRM actuelle**](opm-get-current-hdcp-srm-version.md) à la sortie vidéo. Utilisez la procédure décrite dans la rubrique [envoi de demandes d’État OPM](#sending-opm-status-requests). Cette demande d’État n’a pas de données d’entrée, donc le contenu du membre **abParameters** de la structure des paramètres de l' [**extraction d' \_ \_ informations \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) n’est pas défini.
5.  Quand la méthode [**IOPMVideoOutput :: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) retourne, le tableau **abRequestedInformation** dans la structure d' [**\_ \_ informations demandée par OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) contient une structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . Le membre **ulInformation** de cette structure contient le numéro de version du SRM actuel. Cette valeur doit être égale à la valeur de l’étape 2.

### <a name="enabling-hdcp"></a>Activation de HDCP

Pour activer HDCP, procédez comme suit.

1.  Initialisez une structure de paramètres de niveau de protection de l' [**\_ ensemble \_ \_ \_ OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) avec les valeurs suivantes :
    -   **ulProtectionType**  =  **OPM \_ TYPE de PROTECTION \_ \_ HDCP**
    -   **ulProtectionLevel**  =  **OPM \_ HDCP \_ sur**
    -   **Réservé** = 0
    -   **Reserved2** = 0
2.  Envoie une commande de [**\_ niveau de \_ protection \_ de jeu OPM**](opm-set-protection-level.md) . Les données d’entrée dans le tableau **abParameters** sont la structure des paramètres de niveau de protection de l' [**\_ ensemble \_ \_ \_ OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) .
3.  Envoyer une demande [**OPM \_ obtenir le \_ \_ \_ niveau de protection virtuel**](opm-get-virtual-protection-level.md) pour vérifier si HDCP est activé. Les 4 premiers octets du membre **abParameters** de la structure des paramètres de l’extraction de l' [**\_ \_ information \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) contiennent la valeur de **\_ protection OPM \_ type \_ HDCP**.

Lorsque la méthode [**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) retourne, le tableau **abRequestedInformation** dans la structure d' [**\_ \_ informations demandée par OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) contient une structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . Le membre **ulInformation** de cette structure contient une valeur de l’énumération de [**\_ \_ \_ niveau de protection HDCP HDCP**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) . Si la valeur est égale **\_ à OPM HDCP \_ sur**, cela signifie que HDCP est activé. Sinon, répétez les étapes 1 à 2 jusqu’à ce que HDCP soit activé ou qu’une erreur se produise. (N’oubliez pas d’incrémenter le numéro de séquence et de générer à chaque fois un nouveau nombre aléatoire).

Il faut généralement entre 100 et 200 millisecondes pour activer HDCP, mais cela peut prendre plus de temps. Ne partez pas du principe que HDCP est activé tant que vous ne l’avez pas vérifié.

Lorsque l’application finit de regarder du contenu protégé, désactivez la protection HDCP. Les étapes sont les mêmes que pour l’activation de HDCP, mais à l’étape 1, définissez **ulProtectionLevel** sur **OPM \_ HDCP sur \_ désactivé**.

> [!Note]  
> N’activez pas HDCP Si le type de connecteur est le **connecteur OPM de \_ \_ type \_ DisplayPort \_ intégré**. (Voir [**indicateurs de type de connecteur OPM**](opm-connector-type-flags.md).)

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestionnaire de protection de sortie](output-protection-manager.md)
</dt> </dl>

 

 



