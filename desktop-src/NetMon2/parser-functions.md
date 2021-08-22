---
description: Les fonctions d’assistance suivantes sont appelées par des analyseurs.
ms.assetid: 4e9a9314-8d64-46c0-ad98-bdb9dc4c225a
title: Fonctions de l’analyseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d70c3ad44ad809a323af8acde732af3b142759d3686d78c496f47e92cb8e209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676839"
---
# <a name="parser-functions"></a>Fonctions de l’analyseur

Les fonctions d’assistance suivantes sont appelées par des analyseurs.



| Fonction                                                 | Description                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [AddressToString](addresstostring.md)                   | Convertit une adresse en chaîne.                                                                               |
| [LookupByteSetString](lookupbytesetstring.md)           | Récupère la chaîne correspondant à la valeur spécifiée d’un jeu étiqueté.                                    |
| [SetCCInstPtr](setccinstptr.md)                         | Capture un pointeur d’instance de contexte.                                                                           |
| [StringToAddress](stringtoaddress.md)                   | Convertit une chaîne en adresse.                                                                               |
| [VarLenSmallIntToDword](varlensmallinttodword.md)       | Convertit un petit entier de longueur variable en valeur **DWORD**.                                                      |
| [LookupDwordSetString](lookupdwordsetstring.md)         | Récupère la chaîne correspondant à la valeur spécifiée d’un jeu étiqueté.                                    |
| [LookupWordSetString](lookupwordsetstring.md)           | Récupère la chaîne correspondant à la valeur donnée d’un jeu étiqueté.                                      |
| [BERGetHeader](bergetheader.md)                         | Décode un en-tête Choice.                                                                                       |
| [BERGetInteger](bergetinteger.md)                       | Décode un entier encodé BER.                                                                                 |
| [BERGetString](bergetstring.md)                         | Décode une chaîne encodée BER.                                                                                  |
| [CCHeapAlloc](ccheapalloc.md)                           | Alloue de la mémoire en fonction de la capture.                                                                |
| [CCHeapFree](ccheapfree.md)                             | Libère la mémoire allouée par la fonction **CCHeapAlloc** .                                                 |
| [CCHeapReAlloc](ccheaprealloc.md)                       | Réalloue la mémoire allouée par la fonction **CCHeapAlloc** .                                                  |
| [CCHeapSize](ccheapsize.md)                             | Récupère la taille de la mémoire allouée par la fonction **CCHeapAlloc** .                                    |
| [GetCCInstPtr](getccinstptr.md)                         | Récupère le pointeur vers les données d’instance ajoutées au contexte de capture.                                       |
| [CreateProtocol](createprotocol.md)                     | Informe l’API Moniteur réseau d’existence d’un analyseur de protocole spécifique.                                        |
| [DestroyProtocol](destroyprotocol.md)                   | Détruit le protocole créé par la fonction **CreateProtocol** .                                              |
| [BuildINIPath](buildinipath.md)                         | Récupère un chemin d’accès complet au fichier d’initialisation (INI) qui correspond aux informations que vous entrez.   |
| [CreateHandoffTable](createhandofftable.md)             | Crée une table de remise en fonction des informations contenues dans un fichier INI donné.                                             |
| [DestroyHandoffTable](destroyhandofftable.md)           | Détruit une table de remise créée avec la fonction **CreateHandoffTable** .                                     |
| [GetProtocolFromTable](getprotocolfromtable.md)         | Récupère le protocole d’une table de remise donnée.                                                               |
| [AddProperty](/previous-versions/bb251873(v=msdn.10))                           | Ajoute une structure **PROPERTYINFO** à la base de données des propriétés.                                                    |
| [AttachPropertyInstance](attachpropertyinstance.md)     | Attache une instance de propriété à un frame.                                                                       |
| [AttachPropertyInstanceEx](attachpropertyinstanceex.md) | Attache une instance de propriété à un frame.                                                                       |
| [CreatePropertyDatabase](createpropertydatabase.md)     | Crée une base de données de propriétés qui décrit les propriétés utilisées par l’analyseur pour décrire ses données.               |
| [DestroyPropertyDatabase](destroypropertydatabase.md)   | Détruit une base de données de propriétés créée par des appels aux fonctions **CreatePropertyDatabase** et **AddProperty** . |
| [FindNextFrame](findnextframe.md)                       | Recherche le frame suivant dans le contexte de capture actuel qui correspond à un filtre donné.                               |
| [FindPreviousFrame](findpreviousframe.md)               | Recherche le frame précédent dans le contexte de capture actuel qui correspond à un filtre donné.                           |
| [FormatPropertyInstance](formatpropertyinstance.md)     | Met en forme l’instance de propriété de manière générique.                                                             |
| [GetFrameDestAddress](getframedestaddress.md)           | Récupère l’adresse de destination d’un frame.                                                                  |
| [GetFrameSourceAddress](getframesourceaddress.md)       | Récupère l’adresse source d’un frame.                                                                       |
| [GetProtocolStartOffset](getprotocolstartoffset.md)     | Récupère le décalage d’un protocole donné dans le frame.                                                         |
| [ParserTemporaryLockFrame](parsertemporarylockframe.md) | Verrouille un frame lorsqu’il entre dans un analyseur et déverrouille le frame lorsqu’il s’arrête.                                     |



 

Pour plus d’informations sur les fonctions d’exportation (fonctions d’assistance qui peuvent être appelées par des experts et des analyseurs), des structures et des énumérations, consultez les rubriques suivantes.



| Pour obtenir des informations sur                                  | Consultez                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------|
| Fonctions que les analyseurs exportent.                         | [Fonctions d’exportation de DLL de l’analyseur](parser-dll-export-functions.md)               |
| Structures utilisées par les fonctions d’analyseur.                  | [Structures de l’analyseur](parser-structures.md)                                   |
| Fonctions d’assistance courantes que les analyseurs et les experts appellent. | [Fonctions courantes des experts et de l’analyseur](expert-and-parser-common-functions.md) |



 

 

 
