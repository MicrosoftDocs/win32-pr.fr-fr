---
description: Cette section décrit les fonctions IMM.
ms.assetid: 833c07eb-0ecf-41e2-9e01-8d83e51ffcef
title: Fonctions du gestionnaire de méthode d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 516a83e207434f5d8c2e073e770c878198bc98e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527504"
---
# <a name="input-method-manager-functions"></a>Fonctions du gestionnaire de méthode d’entrée

Cette section décrit les fonctions IMM.



| Fonction                                                           | Description                                                                                                                |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**CreateIFECommonInstance**](/windows/desktop/api/msime/nf-msime-createifecommoninstance)         | Retourne un pointeur vers une interface [**IFECommon**](/windows/desktop/api/Msime/nn-msime-ifecommon) .                                                          |
| [**CreateIFEDictionaryInstance**](/windows/desktop/api/msime/nf-msime-createifedictionaryinstance) | Retourne un pointeur vers une interface [**IFEDictionary**](/windows/desktop/api/Msime/nn-msime-ifedictionary) .                                                  |
| [**CreateIFELanguageInstance**](/windows/desktop/api/msime/nf-msime-createifelanguageinstance)     | Retourne un pointeur vers une interface [**IFELanguage**](/windows/desktop/api/Msime/nn-msime-ifelanguage) .                                                      |
| [**EnumInputContext**](/windows/desktop/api/Imm/nc-imm-imcenumproc)                       | Fonction de rappel définie par l’application qui traite les contextes d’entrée fournis par la fonction **ImmEnumInputContext** .   |
| [**EnumRegisterWordProc**](/windows/desktop/api/Imm/nc-imm-registerwordenumproca)               | Fonction de rappel définie par l’application utilisée avec la fonction **ImmEnumRegisterWord** .                                   |
| [**ImmAssociateContext**](/windows/desktop/api/Imm/nf-imm-immassociatecontext)                 | Associe le contexte d’entrée spécifié à la fenêtre spécifiée.                                                          |
| [**ImmAssociateContextEx**](/windows/desktop/api/Imm/nf-imm-immassociatecontextex)             | Modifie l’association entre le contexte de méthode d’entrée et la fenêtre spécifiée ou ses enfants.                         |
| [**ImmConfigureIME**](/windows/desktop/api/Imm/nf-imm-immconfigureimea)                         | Affiche la boîte de dialogue de configuration de l’IME de l’identificateur de paramètres régionaux d’entrée spécifié.                                |
| [**ImmCreateContext**](/windows/desktop/api/Imm/nf-imm-immcreatecontext)                       | Crée un nouveau contexte d’entrée, en allouant de la mémoire pour le contexte et en l’initialisant.                                        |
| [**ImmDestroyContext**](/windows/desktop/api/Imm/nf-imm-immdestroycontext)                     | Libère le contexte d’entrée et libère la mémoire associée.                                                                    |
| [**ImmDisableIME**](/windows/desktop/api/Imm/nf-imm-immdisableime)                             | Désactive l’IME pour un thread ou pour tous les threads d’un processus.                                                             |
| [**ImmDisableLegacyIME**](/windows/desktop/api/Imm/nf-imm-immdisablelegacyime)                 | Indique que ce thread est un thread d’interface utilisateur d’application du Windows Store.                                                               |
| [**ImmDisableTextFrameService**](/windows/desktop/api/Imm/nf-imm-immdisabletextframeservice)   | Action déconseillée. Désactive le service de texte pour le thread spécifié.                                                            |
| [**ImmEnumInputContext**](/windows/desktop/api/Imm/nf-imm-immenuminputcontext)                 | Récupère le contexte d’entrée pour le thread spécifié.                                                                      |
| [**ImmEnumRegisterWord**](/windows/desktop/api/Imm/nf-imm-immenumregisterworda)                 | Énumère les chaînes de Registre ayant la chaîne de lecture, le style et la chaîne de Registre spécifiés.                           |
| [**ImmEscape**](/windows/desktop/api/Imm/nf-imm-immescapea)                                     | Accède à des fonctionnalités d’IME spécifiques qui ne sont pas disponibles via d’autres fonctions de l’API IME.                           |
| [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)                 | Récupère une liste de candidats.                                                                                                |
| [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)       | Récupère la taille des listes de candidats.                                                                                 |
| [**ImmGetCandidateWindow**](/windows/desktop/api/Imm/nf-imm-immgetcandidatewindow)             | Récupère des informations sur la fenêtre candidats.                                                                         |
| [**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta)             | Récupère des informations sur la police logique actuellement utilisée pour afficher des caractères dans la fenêtre de composition.               |
| [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)         | Récupère des informations sur la chaîne de composition.                                                                        |
| [**ImmGetCompositionWindow**](/windows/desktop/api/Imm/nf-imm-immgetcompositionwindow)         | Récupère des informations sur la fenêtre de composition.                                                                        |
| [**ImmGetContext**](/windows/desktop/api/Imm/nf-imm-immgetcontext)                             | Récupère le contexte d’entrée associé à la fenêtre spécifiée.                                                          |
| [**ImmGetConversionList**](/windows/desktop/api/Imm/nf-imm-immgetconversionlista)               | Récupère la liste des résultats de conversion de caractères ou de mots sans générer de messages liés à l’éditeur IME.                   |
| [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)           | Récupère l’état de conversion actuel.                                                                                   |
| [**ImmGetDefaultIMEWnd**](/windows/desktop/api/Imm/nf-imm-immgetdefaultimewnd)                 | Récupère le handle de fenêtre par défaut de la classe IME.                                                                      |
| [**ImmGetDescription**](/windows/desktop/api/Imm/nf-imm-immgetdescriptiona)                     | Copie la description de l’IME dans la mémoire tampon spécifiée.                                                                 |
| [**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea)                         | Récupère des informations sur les erreurs.                                                                                        |
| [**ImmGetIMEFileName**](/windows/desktop/api/Imm/nf-imm-immgetimefilenamea)                     | Récupère le nom de fichier de l’IME associé aux paramètres régionaux d’entrée spécifiés.                                             |
| [**ImmGetImeMenuItems**](/windows/desktop/api/Imm/nf-imm-immgetimemenuitemsa)                   | Récupère les éléments de menu qui sont enregistrés dans le menu IME d’un contexte d’entrée spécifié.                                 |
| [**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus)                       | Détermine si l’IME est ouvert ou fermé.                                                                              |
| [**ImmGetProperty**](/windows/desktop/api/Imm/nf-imm-immgetproperty)                           | Récupère la propriété et les fonctionnalités de l’IME associé aux paramètres régionaux d’entrée spécifiés.                             |
| [**ImmGetRegisterWordStyle**](/windows/desktop/api/Imm/nf-imm-immgetregisterwordstylea)         | Récupère une liste des styles pris en charge par l’IME associé aux paramètres régionaux d’entrée spécifiés.                            |
| [**ImmGetStatusWindowPos**](/windows/desktop/api/Imm/nf-imm-immgetstatuswindowpos)             | Récupère la position de la fenêtre d’État.                                                                               |
| [**ImmGetVirtualKey**](/windows/desktop/api/Imm/nf-imm-immgetvirtualkey)                       | Récupère la valeur de clé virtuelle d’origine associée à un message d’entrée de clé que l’IME a déjà traité.           |
| [**ImmInstallIME**](/windows/desktop/api/Imm/nf-imm-imminstallimea)                             | Installe un IME.                                                                                                           |
| [**ImmIsIME**](/windows/desktop/api/Imm/nf-imm-immisime)                                       | Détermine si les paramètres régionaux d’entrée spécifiés ont un IME.                                                                       |
| [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)                           | Recherche les messages destinés à la fenêtre IME et les envoie à la fenêtre spécifiée.                          |
| [**ImmNotifyIME**](/windows/desktop/api/Imm/nf-imm-immnotifyime)                               | Notifie l’IME des modifications apportées à l’état du contexte d’entrée.                                                         |
| [**ImmRegisterWord**](/windows/desktop/api/Imm/nf-imm-immregisterworda)                         | Inscrit une chaîne avec le dictionnaire de l’IME associé aux paramètres régionaux d’entrée spécifiés.                              |
| [**ImmReleaseContext**](/windows/desktop/api/Imm/nf-imm-immreleasecontext)                     | Libère le contexte d’entrée et déverrouille la mémoire associée dans le contexte d’entrée.                                         |
| [**ImmRequestMessage**](/windows/desktop/api/Immdev/nf-immdev-immrequestmessagea)                     | Demande un message de l’application.                                                                                   |
| [**ImmSetCandidateWindow**](/windows/desktop/api/Imm/nf-imm-immsetcandidatewindow)             | Définit des informations sur la fenêtre candidats.                                                                              |
| [**ImmSetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immsetcompositionfonta)             | Définit la police logique à utiliser pour afficher les caractères dans la fenêtre de composition.                                              |
| [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa)         | Définit les caractères, les attributs et les clauses des chaînes de composition et de lecture.                                       |
| [**ImmSetCompositionWindow**](/windows/desktop/api/Imm/nf-imm-immsetcompositionwindow)         | Définit la position de la fenêtre de composition.                                                                               |
| [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus)           | Définit l’état de la conversion actuelle.                                                                                        |
| [**ImmSetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immsetopenstatus)                       | Ouvre ou ferme l’IME.                                                                                                   |
| [**ImmSetStatusWindowPos**](/windows/desktop/api/Imm/nf-imm-immsetstatuswindowpos)             | Définit la position de la fenêtre d’État.                                                                                    |
| [**ImmSimulateHotKey**](/windows/desktop/api/Imm/nf-imm-immsimulatehotkey)                     | Simule la touche d’accès rapide IME spécifiée, provoquant la même réponse que si l’utilisateur appuie sur la touche d’accès rapide dans la fenêtre spécifiée. |
| [**ImmUnregisterWord**](/windows/desktop/api/Imm/nf-imm-immunregisterworda)                     | Supprime une chaîne de Registre du dictionnaire de l’IME associé aux paramètres régionaux d’entrée spécifiés.                       |



 

 

 



