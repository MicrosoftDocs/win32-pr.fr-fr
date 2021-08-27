---
description: La session de suivi d’événements de journalisation globale enregistre les événements qui se produisent au début du processus de démarrage du système d’exploitation.
ms.assetid: 1462bbef-ef32-4053-9930-5b4a0ab46b47
title: Configuration et démarrage de la session de journalisation globale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a928cba5eb782ca4a57f7dba4776de79f42d7af
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477045"
---
# <a name="configuring-and-starting-the-global-logger-session"></a>Configuration et démarrage de la session de journalisation globale

La session de suivi d’événements de journalisation globale enregistre les événements qui se produisent au début du processus de démarrage du système d’exploitation. Les applications et les pilotes de périphériques peuvent utiliser la session d’enregistreur d’événements globale pour capturer des suivis avant que l’utilisateur se connecte. Notez que certains pilotes de périphérique, tels que les pilotes de périphériques de disque, ne sont pas chargés au moment où la session de journalisation globale commence.

> [!Note]  
> si vous créez une session de journalisation globale sur Windows Vista, vous devez envisager de créer une [session de journalisation](configuring-and-starting-an-autologger-session.md) automatique à la place.

 

Vous utilisez le registre pour configurer la session d’enregistreur d’événements globale. Ajoutez la clé **GlobalLogger** à la clé de Registre suivante, si elle n’est pas déjà présente :

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
```

Le tableau suivant décrit les valeurs que vous pouvez définir pour la clé **GlobalLogger** . Vous devez disposer de privilèges d’administrateur pour spécifier ces valeurs de registre. Les valeurs de Registre affectent tous les fournisseurs qui consignent des événements dans la session de journalisation globale. La valeur de **départ** est la seule valeur requise pour démarrer la session d’enregistreur d’événements globale ; toutes les autres valeurs ont des paramètres par défaut qui sont utilisés si la valeur n’est pas présente dans le registre. En règle générale, vous devez utiliser les valeurs par défaut. Si vous spécifiez une valeur que ETW ne peut pas prendre en charge, ETW remplace la valeur.




| Valeur | Type | Description | 
|-------|------|-------------|
| <strong>Start</strong> | <strong>REG_DWORD</strong> | Définissez cette valeur sur 1 (activé) pour démarrer la session d’enregistreur d’événements globale lors du prochain démarrage du système. Pour arrêter le démarrage de la session, définissez cette valeur sur 0 (désactivé). <br /> | 
| <strong>BufferSize</strong> | <strong>REG_DWORD</strong> | Taille de chaque mémoire tampon, en kilo-octets. Cette valeur doit être inférieure à un mégaoctet. ETW utilise la taille de la mémoire physique pour calculer cette valeur. <br /> | 
| <strong>ClockType</strong> | <strong>REG_DWORD</strong> | Minuteur à utiliser lors de la journalisation de l’horodatage pour chaque événement.<ul><li>1 = valeur de compteur de performance (haute résolution)</li><li>2 = minuterie du système</li><li>3 = compteur du cycle de l’UC</li></ul>Pour obtenir une description de chaque type d’horloge, consultez le membre <strong>ClientContext</strong> de <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.<br /> la valeur par défaut est 1 (valeur du compteur de performances) sur Windows Vista et versions ultérieures. avant Windows Vista, la valeur par défaut est 2 (horloge système).<br /> | 
| <strong>EnableKernelFlags</strong> | <strong>REG_BINARY</strong> | Utilisez cette valeur pour activer un ou plusieurs fournisseurs de noyau. Si vous activez les fournisseurs de noyau, la session de journalisation globale se renomme en journal de noyau NT au démarrage. Pour connaître les valeurs possibles, consultez le membre <strong>EnableFlags</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>.<br /> | 
| <strong>FileCounter</strong> | <strong>REG_DWORD</strong> | Nombre de fichiers journaux des traces d’événements générés par les sessions globales du journal. Le système incrémente cette valeur jusqu’à ce qu’elle atteigne la valeur de <strong>FileMax</strong>. Ensuite, il réinitialise la valeur à 0. Ce compteur empêche le système de remplacer un fichier journal de suivi du journal global. <br /> | 
| <strong>FileMax</strong> | <strong>REG_DWORD</strong> | Nombre maximal de fichiers journaux de suivi d’événements autorisés sur le système. Lorsque le nombre de journaux de suivi atteint la valeur maximale spécifiée, le système commence à remplacer les journaux, en commençant par le plus ancien. <br /> Si le fichier journal spécifié dans <strong>filename</strong> existe, ETW ajoute la valeur <strong>FileCounter</strong> au nom de fichier. Par exemple, si le nom du fichier journal par défaut est utilisé, le formulaire est%SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl.NNNN. <br /> La valeur par défaut est 0, ce qui signifie qu’il n’y a pas de valeur maximale. <br /> | 
| <strong>FileName</strong> | <strong>REG_SZ</strong> | Chemin complet du fichier journal. Le chemin d’accès à ce fichier doit exister. Le fichier journal est un fichier journal séquentiel. Notez que tous les fournisseurs qui écrivent des événements dans la session d’enregistreur d’événements globale écrivent des événements dans ce fichier journal. Le chemin d’accès est limité à 1024 caractères. Si <strong>filename</strong> n’est pas spécifié, les événements sont écrits dans%SystemRoot%\System32\LogFiles\WMI\GlobalLogger.etl. <strong>avant Windows Vista :</strong> Le fichier par défaut est%SystemRoot%\System32\LogFiles\WMI\Trace.log.<br /><br /> | 
| <strong>FlushTimer</strong> | <strong>REG_DWORD</strong> | Fréquence, en secondes, de vidage forcé des mémoires tampons de trace. La durée de vidage minimale est de 1 seconde. Ce vidage forcé s’ajoute au vidage automatique qui se produit lorsqu’une mémoire tampon est saturée et lorsque la session de trace s’arrête. <br /> Dans le cas d’un enregistreur d’événements en temps réel, la valeur zéro (valeur par défaut) signifie que le temps de vidage sera défini sur 1 seconde. Un enregistreur d’événements en temps réel est lorsque <strong>LogFileMode</strong> a la valeur <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br /> La valeur par défaut est 0. Par défaut, les mémoires tampons sont vidées uniquement lorsqu’elles sont pleines. <br /> | 
| <strong>LogFileMode</strong> | <strong>REG_DWORD</strong> | Spécifie les options de session de journal. Pour les valeurs, consultez <a href="logging-mode-constants.md">constantes de mode de journalisation</a>. cette valeur est prise en charge sur Windows Vista et versions ultérieures. <br /> | 
| <strong>MaximumBuffers</strong> | <strong>REG_DWORD</strong> | Nombre maximal de mémoires tampons à allouer. En général, cette valeur est le nombre minimal de mémoires tampons plus vingt. ETW utilise la taille de la mémoire tampon et la taille de la mémoire physique pour calculer cette valeur. Cette valeur doit être supérieure ou égale à la valeur de <strong>MinimumBuffers</strong>.<br /> | 
| <strong>MaxFileSize</strong> | <strong>REG_DWORD</strong> | Taille maximale, en mégaoctets, du fichier journal de suivi d’événements. Par défaut, il n’y a pas de taille de fichier maximale.<br /> | 
| <strong>MinimumBuffers</strong> | <strong>REG_DWORD</strong> | Nombre minimal de mémoires tampons à allouer au démarrage de la session de journalisation globale. Le nombre minimal de mémoires tampons que vous pouvez spécifier est deux mémoires tampons par processeur. Par exemple, sur un ordinateur à processeur unique, le nombre minimal de mémoires tampons est de deux. <br /> La valeur par défaut sur un système à processeur unique est 0x3.<br /> | 
| <strong>Statut</strong> | <strong>REG_DWORD</strong> | État de démarrage de l’enregistreur d’événements global. Si le journal global n’a pas pu démarrer, la valeur de cette clé est le code d’erreur Win32 approprié. Si le journal Global a démarré, la valeur de cette clé est ERROR_SUCCESS (0).<br /> | 




 

Une fois que le registre a été modifié et que l’ordinateur a redémarré, la session de journalisation globale démarre automatiquement et est utilisée comme toute autre session, à une exception près : vous utilisez le \_ handle de constante d’ID de journal Global WMI \_ \_ (défini dans Wmistr. h) pour référencer la session d’enregistreur d’événements globale. Cette constante peut être utilisée comme argument pour toute fonction de suivi d’événement qui accepte un handle de session. Dans les fonctions qui acceptent un nom de session, utilisez le nom d’enregistreur d’événements GLOBAL \_ \_ .

Le contrôleur d’enregistreur d’événements global n’appelle pas la fonction [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) pour activer les fournisseurs. Le fournisseur est chargé de déterminer si la session de journalisation globale est démarrée, puis de s’activer.

Pour déterminer si la session de journalisation globale est démarrée, vous pouvez appeler la fonction [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) , en affectant à *SessionHandle* la valeur \_ ID d’enregistreur d’événements global WMI \_ et ControlCode la valeur de la \_  **requête de contrôle de trace d’événements \_ \_ \_**. Si l’appel **ControlTrace** réussit, la session de journalisation globale existe et le fournisseur peut s’activer lui-même et consigner des événements dans la session de journalisation globale (la fonction **CONTROLTRACE** renvoie une erreur \_ \_ instance WMI \_ \_ introuvable si le journal global n’est pas actif).

En règle générale, le contrôleur est chargé de passer les indicateurs d’activation et le niveau au fournisseur lorsqu’il active le fournisseur, mais comme le contrôleur d’enregistreur global n’active pas le fournisseur, il incombe au fournisseur de transmettre ces informations à lui-même, si nécessaire.

La session de journalisation globale est une ressource limitée et doit être utilisée avec modération. Les services qui souhaitent capturer des informations pendant le processus de démarrage doivent envisager d’ajouter la logique du contrôleur à lui-même au lieu d’utiliser la session d’enregistreur d’événements globale.

Pour plus d’informations sur le démarrage d’une session de suivi d’événements, consultez [configuration et démarrage d’une session de suivi d’événements](configuring-and-starting-an-event-tracing-session.md).

Pour plus d’informations sur le démarrage d’une session privée de journalisation, consultez [configuration et démarrage d’une session de journalisation privée](configuring-and-starting-a-private-logger-session.md).

Pour plus d’informations sur le démarrage d’une session de journal de noyau NT, consultez [configuration et démarrage de la session de journalisation du noyau NT](configuring-and-starting-the-nt-kernel-logger-session.md).

