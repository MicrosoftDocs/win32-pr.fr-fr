---
description: Les fichiers journaux WMI ne sont plus pris en charge.
ms.assetid: 4ba80063-7aa6-42df-a620-1b366b795034
ms.tgt_platform: multiple
title: Journalisation de l’activité WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ced8645eb7ad9005e6ba751d011ae7f0ccb3dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527665"
---
# <a name="logging-wmi-activity"></a>Journalisation de l’activité WMI

Les fichiers journaux WMI ne sont plus pris en charge. À compter de Windows Vista, WMI utilise [suivi d’v nements pour Windows (ETW](/windows/desktop/ETW/event-tracing-portal)) et les événements qui sont disponibles via l’interface utilisateur **Observateur d’événements** ou l’outil en ligne de commande Wevtutil. Pour plus d’informations, consultez le fournisseur ETW et la documentation de la ligne de commande [wevutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732848(v=ws.11)) .

Les sections suivantes sont présentées dans cette rubrique :

-   [Fichiers journaux WMI avant Windows Vista](#wmi-log-files-before-windows-vista)
-   [Journalisation des activités pour les composants WMI Core avant Windows Vista](#logging-activities-for-wmi-core-components-before-windows-vista)
-   [Journalisation des activités pour les composants du fournisseur WMI avant Windows Vista](#logging-activities-for-wmi-provider-components-before-windows-vista)
-   [Rubriques connexes](#related-topics)

## <a name="wmi-log-files-before-windows-vista"></a>Fichiers journaux WMI avant Windows Vista

Les fichiers journaux créés par WMI et différents fournisseurs enregistrent les événements, les données de trace ou de diagnostic, les erreurs et diverses activités. Seuls les administrateurs ont accès en lecture au dossier du journal WMI situé dans les \\ journaux WBEM% windir% system32 \\ \\ .

Seuls les composants WMI Core ou les fournisseurs WMI écrivent dans les fichiers journaux. Vous pouvez uniquement lire ou afficher les données de ces journaux à des fins de diagnostic. Vous pouvez créer et stocker vos propres fichiers journaux dans le répertoire des journaux WMI.

## <a name="logging-activities-for-wmi-core-components-before-windows-vista"></a>Journalisation des activités pour les composants WMI Core avant Windows Vista

Ces fichiers ne contiennent pas un format cohérent qui convient pour la lecture par programme. Pour plus d’informations sur des journaux spécifiques, consultez [fichiers journaux WMI](wmi-log-files.md).

Les activités de journalisation pour les composants WMI Core se produisent lorsque les clés de Registre suivantes sont définies :

-   Niveau de journalisation

    Les modifications apportées à la valeur de Registre du niveau de journalisation prennent effet immédiatement. Aucun redémarrage du service WMI n’est nécessaire.

    **HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\  \\  \\  \\ **journalisation** CIMOM Microsoft WBEM = 2

    La liste suivante répertorie les niveaux de journalisation qui peuvent être définis dans le registre.

    

    | Niveau de journalisation | Description               |
    |---------------|---------------------------|
    | 0             | Aucune journalisation                |
    | 1             | Journaliser uniquement les erreurs           |
    | 2             | Journalisation détaillée (par défaut) |

    

     

-   Emplacement du fichier journal

    Pour que les modifications apportées à l’emplacement du fichier journal prennent effet, redémarrez le service WMI.

    **HKEY \_ Logiciel d' \_ ordinateur local** répertoire de \\  \\  \\  \\  \\ **journalisation** CIMOM Microsoft WBEM =% windir% \\ system32 \\ \\ journaux WBEM

-   Taille maximale du fichier journal, en octets

    **HKEY \_ \_Ordinateur local** \\ **logiciel** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **fichier journal CIMOM taille maximale** = 65536

Vous pouvez modifier ces valeurs de clé de Registre par le biais de l’éditeur du registre ou via le composant logiciel enfichable WMI de la console MMC (Microsoft Management Console).

**Pour définir le niveau de journalisation pour WMI avant Windows Vista**

1.  Cliquez sur **Démarrer**, puis sur **Exécuter**.
2.  Tapez **wmimgmt. msc**
3.  Dans le menu **Action**, cliquez sur **Propriétés**.
4.  Sous l’onglet **journalisation** , définissez le niveau de journalisation sur **désactivé**, **activé** ou **détaillé**.
5.  Dans **emplacement :**, tapez le chemin d’accès au dossier du fichier journal et, dans **taille maximale (octets) :**, définissez la taille maximale, en octets, du fichier journal.

Pour plus d’informations sur la définition des propriétés du fichier journal, consultez l’aide en ligne de l’application de contrôle WMI.

## <a name="logging-activities-for-wmi-provider-components-before-windows-vista"></a>Journalisation des activités pour les composants du fournisseur WMI avant Windows Vista

Lorsque la journalisation des composants principaux de WMI est activée, l’enregistrement est également activé pour n’importe quel fournisseur avec des fonctionnalités de journalisation.

La liste suivante répertorie les valeurs requises.

<dl> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>**Txt**
</dt> <dd>

Chemin d’accès complet et nom de fichier du fichier journal. La valeur par défaut est% windir% \\ system32 \\ WBEM \\ logs. La valeur nommée du **type** doit être définie sur = file pour cette valeur nommée à utiliser.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>**Niveau**
</dt> <dd>

Masque logique 32 bits qui définit le type de sortie de débogage générée par le fournisseur. Cette valeur dépend du fournisseur. La valeur par défaut est 0 (zéro).

</dd> <dt>

<span id="MaxFileSize"></span><span id="maxfilesize"></span><span id="MAXFILESIZE"></span>**MaxFileSize**
</dt> <dd>

Taille de fichier maximale, en octets, du fichier journal. Cette valeur entière doit être comprise entre 1024 et 2 ^ 32-1. Lorsque la taille du fichier dépasse cette valeur, le fichier est renommé en **~ filename** et un nouveau fichier journal vide est créé. L’espace disque requis pour le fichier journal est le double de la valeur de **MaxFileSize**. La valeur par défaut est 65 535.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Entrer**
</dt> <dd>

Peut avoir la valeur = file ou = Debugger. Si la valeur est = file, les informations de trace sont écrites dans le fichier journal spécifié dans le **fichier** nommé value. La valeur par défaut est = file.

</dd> </dl>

Par exemple, pour consigner une requête et obtenir des appels d’instance à partir du fournisseur de vues, utilisez les valeurs de clés de Registre suivantes. Le journal se trouvera dans le dossier log et sera la taille de fichier par défaut.

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\  \\ connexion des fournisseurs WBEM Microsoft \\  \\  \\ **ViewProvider** \\ **fichier** = C : \\ Windows \\ system32 \\ WBEM \\ journaux \\ ViewProvider. log

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\  \\ connexion des fournisseurs **WBEM Microsoft WBEM** \\  \\  \\  \\ **niveau** ViewProvider = 2

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\  \\ connexion des fournisseurs WBEM Microsoft \\  \\  \\ **ViewProvider** \\ **MaxFileSize** = 65535

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\  \\  \\ journalisation des **fournisseurs** Microsoft WBEM \\  \\ **ViewProvider** \\ **type** = fichier

> [!Note]  
> Pour vos propres fournisseurs avec des fonctionnalités de journalisation, vous devez écrire les clés et valeurs de Registre nécessaires pour activer la journalisation.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes WMI](wmi-troubleshooting.md)
</dt> <dt>

[Fichiers journaux WMI](wmi-log-files.md)
</dt> <dt>

[Classes de résolution des problèmes WMI](wmi-troubleshooting-classes.md)
</dt> <dt>

[Suivi de l’activité WMI](tracing-wmi-activity.md)
</dt> </dl>

 

 
