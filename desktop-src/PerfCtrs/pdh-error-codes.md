---
description: Toutes les fonctions d’assistance de données de performances (PDH) retournent une valeur de type PDH \_ Status.
ms.assetid: ea67d798-81db-44ad-b0fb-24e0c3be7388
title: Codes d’erreur de l’application d’assistance pour les données de performances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16367cb3cd2c0ed83c69067e82fe180a6930910b1c45e76d3e01b75a6832d89a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033809"
---
# <a name="performance-data-helper-error-codes"></a>Codes d’erreur de l’application d’assistance pour les données de performances

Toutes les fonctions d’assistance de données de performances (PDH) retournent une valeur de type **PDH \_ Status**. Si la fonction est réussie, la valeur de retour est `ERROR_SUCCESS` . Dans le cas contraire, la fonction retourne un [code d’erreur système](/windows/desktop/Debug/system-error-codes) ou un code d’erreur PDH. Pour récupérer le texte de description de l’erreur dans votre application, utilisez la fonction [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) comme indiqué dans l’exemple suivant.

```C++
#include <windows.h>
#include <stdio.h>
#include <pdhmsg.h>

void main(void)
{
    HANDLE hPdhLibrary = NULL;
    LPWSTR pMessage = NULL;
    DWORD dwErrorCode = PDH_PLA_ERROR_ALREADY_EXISTS;

    hPdhLibrary = LoadLibrary(L"pdh.dll");
    if (NULL == hPdhLibrary)
    {
        wprintf(L"LoadLibrary failed with %lu\n", GetLastError());
        return;
    }

    if (!FormatMessage(FORMAT_MESSAGE_FROM_HMODULE |
                       FORMAT_MESSAGE_ALLOCATE_BUFFER |
                       FORMAT_MESSAGE_IGNORE_INSERTS,
                       hPdhLibrary,
                       dwErrorCode,
                       0,
                       (LPWSTR)&pMessage,
                       0,
                       NULL))
    {
        wprintf(L"Format message failed with 0x%x\n", GetLastError());
        return;
    }

    wprintf(L"Formatted message: %ls\n", pMessage);
    LocalFree(pMessage);
}
```

Pour la collecte de données et les fonctions de mise en forme, il est important de se souvenir que la valeur de retour de la fonction indique la réussite ou l’erreur de l’appel de fonction et pas nécessairement celle des données de compteur. Vérifiez toujours le membre **CStatus** de la valeur de compteur retournée pour vous assurer que les données retournées sont valides avant de l’utiliser. Si la valeur du membre **CStatus** n’indique pas de réussite, n’utilisez pas les données.

Le tableau suivant fournit la liste des codes d’erreur spécifiques à PDH. Ces valeurs sont définies dans le `pdhmsg.h` fichier d’en-tête.

| Code d'erreur                                                   | Description
|--------------------------------------------------------------|------------
| 0x00000000 ( \_ \_ données valides PDH CSTATUS \_ )                       | Les données retournées sont valides.
| 0x00000001 (PDH \_ CSTATUS \_ nouvelles \_ données)                         | La valeur des données de retour est valide et différente de celle du dernier échantillon.
| 0x800007D0 (PDH \_ CSTATUS \_ non \_ machine)                       | Impossible de se connecter à l’ordinateur spécifié ou l’ordinateur est hors connexion.
| 0x800007D1 (PDH \_ CSTATUS \_ aucune \_ instance)                      | L’instance spécifiée n’est pas présente.
| 0x800007D2 (PDH \_ plus de \_ données)                                 | Il y a plus de données à retourner que dans la mémoire tampon fournie. Allouez une mémoire tampon plus grande et rappelez la fonction.
| 0x800007D3 ( \_ élément CSTATUS \_ PDH \_ non \_ validé)              | L’élément de données a été ajouté à la requête, mais n’a pas été validé ni accédé. Aucune autre information sur l’état de cet élément de données n’est disponible.
| 0x800007D4 ( \_ nouvelle tentative PDH)                                      | L’opération sélectionnée doit être retentée.
| 0x800007D5 (PDH \_ aucune \_ donnée)                                   | Aucune donnée à retourner.
| 0x800007D6 ( \_ dénominateur Calc \_ négatif Calc \_ )                | Un compteur avec une valeur de dénominateur négative a été détecté.
| 0x800007D7 (valeur du temps de \_ calcul négatif du calcul PDH \_ \_ )                   | Un compteur avec une valeur de base de temps négative a été détecté.
| 0x800007D8 ( \_ valeur négative du calcul PDH \_ \_ )                      | Un compteur avec une valeur négative a été détecté.
| 0x800007D9 ( \_ boîte de dialogue PDH \_ annulée)                          | L’utilisateur a annulé la boîte de dialogue.
| 0x800007DA ( \_ fin de la fin \_ du \_ fichier journal PDH \_ )                         | La fin du fichier journal a été atteinte.
| 0x800007DB ( \_ \_ délai d’attente de requête asynchrone PDH \_ )                      | Un dépassement de délai s’est produit lors de l’attente de la fin du thread de collection de compteurs asynchrones.
| 0x800007DC (PDH \_ ne peut pas \_ définir la \_ source de source en \_ temps réel par défaut \_ ) | Impossible de modifier la source de données définie par défaut en temps réel. Des sessions de requête en temps réel collectent des données de compteur.
| 0xC0000BB8 (PDH \_ CSTATUS \_ aucun \_ objet)                        | L’objet spécifié est introuvable sur le système.
| 0xC0000BB9 (PDH \_ CSTATUS \_ aucun \_ compteur)                       | Le compteur spécifié est introuvable.
| 0xC0000BBA (PDH \_ CSTATUS \_ données non valides \_ )                     | Les données retournées ne sont pas valides.
| 0xC0000BBB ( \_ échec d’allocation de mémoire PDH \_ \_ )                | Une fonction PDH n’a pas pu allouer suffisamment de mémoire temporaire pour terminer l’opération. Fermez certaines applications ou étendez le fichier d’échange et recommencez la fonction.
| 0xC0000BBC ( \_ handle PDH non valide \_ )                            | Le descripteur n’est pas un objet PDH valide.
| 0xC0000BBD ( \_ argument non valide PDH \_ )                          | Un argument requis est manquant ou incorrect.
| 0xC0000BBE ( \_ fonction PDH \_ \_ introuvable)                       | Impossible de trouver la fonction spécifiée.
| 0xC0000BBF (PDH \_ CSTATUS \_ non \_ COUNTERNAME)                   | Aucun compteur n’a été spécifié.
| 0xC0000BC0 (PDH \_ CSTATUS \_ mauvais \_ COUNTERNAME)                  | Impossible d’analyser le chemin d’accès du compteur. Vérifiez le format et la syntaxe du chemin d’accès spécifié.
| 0xC0000BC1 ( \_ mémoire tampon PDH non valide \_ )                            | La mémoire tampon passée par l’appelant n’est pas valide.
| 0xC0000BC2 ( \_ mémoire tampon PDH insuffisante \_ )                       | Les données demandées sont supérieures à la mémoire tampon fournie. Impossible de retourner les données demandées.
| 0xC0000BC3 (PDH \_ ne peut pas \_ se connecter à l' \_ ordinateur)                   | Impossible de se connecter à l’ordinateur demandé.
| 0xC0000BC4 ( \_ \_ chemin d’accès PDH non valide)                              | Impossible d’interpréter le chemin d’accès au compteur spécifié.
| 0xC0000BC5 ( \_ instance non valide PDH \_ )                          | Impossible de lire le nom de l’instance à partir du chemin d’accès au compteur spécifié.
| 0xC0000BC6 ( \_ données non valides PDH \_ )                              | Les données ne sont pas correctes.
| 0xC0000BC7 (PDH \_ pas de \_ données de boîte de dialogue \_ )                           | Le bloc de données de la boîte de dialogue est manquant ou non valide.
| 0xC0000BC8 (PDH \_ ne peut pas \_ lire les \_ chaînes de nom \_ )                | Impossible de lire le compteur et/ou le texte d’aide à partir de l’ordinateur spécifié.
| 0xC0000BC9 ( \_ erreur de \_ création de fichier journal PDH \_ \_ )                   | Impossible de créer le fichier journal spécifié.
| 0xC0000BCA ( \_ erreur d' \_ ouverture de fichier journal PDH \_ \_ )                     | Impossible d’ouvrir le fichier journal spécifié.
| 0xC0000BCB ( \_ type de journal PDH \_ \_ \_ introuvable)                      | Le type de fichier journal spécifié n’a pas été installé sur ce système.
| 0xC0000BCC (PDH plus de \_ \_ \_ données)                             | Aucune donnée n'est disponible.
| 0xC0000BCD ( \_ entrée PDH \_ absente \_ dans le \_ \_ fichier journal)                  | L’enregistrement spécifié est introuvable dans le fichier journal.
| 0xC0000BCE (la \_ source de données PDH \_ est un \_ \_ \_ fichier journal)                | La source de données spécifiée est un fichier journal.
| 0xC0000BCF (la \_ source de données PDH \_ \_ est \_ en \_ temps réel)               | La source de données spécifiée est l’activité en cours.
| 0xC0000BD0 (PDH \_ Impossible de \_ lire l' \_ \_ en-tête de journal)                  | Impossible de lire l’en-tête du fichier journal.
| 0xC0000BD1 ( \_ fichier PDH \_ \_ introuvable)                           | Impossible de trouver le fichier spécifié.
| 0xC0000BD2 (le \_ fichier \_ PDH \_ existe déjà)                      | Il existe déjà un fichier avec le nom de fichier spécifié.
| 0xC0000BD3 (PDH \_ non \_ implémenté)                           | La fonction référencée n’a pas été implémentée.
| 0xC0000BD4 ( \_ chaîne PDH \_ \_ introuvable)                         | Impossible de trouver la chaîne spécifiée dans la liste des chaînes de nom de performance et de texte d’aide.
| 0x80000BD5 (PDH \_ ne peut pas \_ mapper les \_ fichiers de noms \_ )                   | Impossible de mapper aux fichiers de données du nom du compteur de performance. Les données seront lues à partir du Registre et stockées localement.
| 0xC0000BD6 ( \_ format de \_ Journal inconnu PDH \_ )                       | Le format du fichier journal spécifié n’est pas reconnu par la DLL PDH.
| 0xC0000BD7 ( \_ commande PDH inconnue \_ LOGSVC \_ )                   | La valeur de commande du service de journalisation spécifiée n’est pas reconnue.
| 0xC0000BD8 ( \_ requête PDH \_ LOGSVC \_ \_ introuvable)                  | La requête spécifiée à partir du service de journalisation est introuvable ou n’a pas pu être ouverte.
| 0xC0000BD9 (PDH \_ LOGSVC \_ non \_ ouvert)                        | Impossible d’ouvrir la clé du service de journalisation des données de performances. Cela peut être dû à un privilège insuffisant ou au fait que le service n’a pas été installé.
| 0xC0000BDA ( \_ erreur WBEM PDH \_ )                                | Une erreur s’est produite lors de l’accès au magasin de données WBEM.
| 0xC0000BDB ( \_ accès PDH \_ refusé)                             | Impossible d’accéder à l’ordinateur ou au service souhaité. Vérifiez les autorisations et l’authentification du service de journalisation ou de la session utilisateur interactive par rapport à celles de l’ordinateur ou du service en cours d’analyse.
| 0xC0000BDC ( \_ fichier journal \_ PDH \_ trop \_ petit)                      | La taille maximale du fichier journal spécifiée est insuffisante pour journaliser les compteurs sélectionnés. Aucune donnée ne sera enregistrée dans ce fichier journal. Spécifiez un plus petit ensemble de compteurs à consigner ou une taille de fichier plus importante, puis recommencez l’appel.
| 0xC0000BDD (une \_ source de source PDH non valide \_ )                        | Impossible de se connecter au nom de la source de source ODBC.
| 0xC0000BDE (PDH \_ non valide \_ SQLDB)                             | SQL Database ne contient pas un jeu de tables valide pour Perfmon.
| 0xC0000BDF (PDH \_ aucun \_ compteur)                               | aucun compteur n’a été trouvé pour ce jeu de journaux de SQL Perfmon.
| 0xC0000BE0 (PDH \_ SQL \_ ALLOC \_ a échoué)                         | Échec de l’appel à SQLAllocStmt, avec %1.
| 0xC0000BE1 (PDH \_ SQL \_ ALLOCCON \_ échec)                      | Échec de l’appel à SQLAllocConnect avec %1.
| 0xC0000BE2 (PDH \_ SQL \_ EXEC \_ DIRECT \_ a échoué)                  | Échec de l’appel à SQLExecDirect avec %1.
| 0xC0000BE3 (échec de l’extraction de l' \_ SQL PDH \_ \_ )                         | Échec de l’appel à SQLFetch avec %1.
| 0xC0000BE4 (PDH \_ SQL \_ ROWCOUNT \_ a échoué)                      | Échec de l’appel à SQLRowCount avec %1.
| 0xC0000BE5 (PDH \_ SQL \_ plus de \_ résultats \_ )                 | Échec de l’appel à SQLMoreResults avec %1.
| 0xC0000BE6 (PDH \_ SQL \_ CONNECT \_ a échoué)                       | Échec de l’appel à SQLConnect avec %1.
| 0xC0000BE7 (échec de la \_ liaison PDH SQL \_ \_ )                          | Échec de l’appel à SQLBindCol avec %1.
| 0xC0000BE8 (PDH \_ ne peut pas \_ connecter le \_ \_ serveur WMI)               | Impossible de se connecter au serveur WMI sur l’ordinateur demandé.
| 0xC0000BE9 ( \_ collection PLA \_ PDH \_ déjà \_ en cours d’exécution)          | Collection « %1 ! s ! » est déjà en cours d’exécution.
| 0xC0000BEA (chevauchement de la \_ planification d’erreur PDH PLA \_ \_ \_ )              | L’heure de début spécifiée est postérieure à l’heure de fin.
| 0xC0000BEB ( \_ collection PLA \_ PDH \_ \_ introuvable)                | Collection « %1 ! s ! » n’existe pas.
| 0xC0000BEC ( \_ planification d’erreur PDH PLA \_ \_ \_ écoulée)              | L’heure de fin spécifiée s’est déjà écoulée.
| 0xC0000BED (PDH \_ PLA \_ erreur \_ nostart)                        | Collection « %1 ! s ! » n’a pas démarré ; Recherchez d’éventuelles erreurs dans le journal des événements de l’application.
| 0xC0000BEE (l' \_ erreur PDH PLA \_ \_ \_ existe déjà)                | Collection « %1 ! s ! » existe déjà.
| 0xC0000BEF ( \_ erreur d' \_ \_ incompatibilité de type d’erreur PDH PLA \_ )                 | Il y a une incompatibilité dans le type de paramètres.
| 0xC0000BF0 (PDH \_ PLA \_ Error \_ filePath)                       | Les informations spécifiées ne correspondent pas à un nom de chemin d’accès valide.
| 0xC0000BF1 ( \_ erreur PDH PLA \_ service \_ )                        | Le service « journaux de performances & alertes » n’a pas répondu.
| 0xC0000BF2 ( \_ erreur de \_ validation PDH PLA \_ )                     | Les informations transmises ne sont pas valides.
| 0x80000BF3 ( \_ avertissement de \_ validation PDH PLA \_ )                   | Les informations transmises ne sont pas valides.
| 0xC0000BF4 (PDH \_ PLA \_ nom d’erreur \_ \_ trop \_ long)                | Le nom fourni est trop long.
| 0xC0000BF5 ( \_ FORMAT de journal de SQL non valide PDH \_ \_ \_ )                  | le format du journal SQL est incorrect. Le format correct est `SQL:<DSN-name>!<LogSet-Name>` .
| 0xC0000BF6 ( \_ compteur PDH \_ déjà \_ dans la \_ requête)                | Le compteur de performances de l’appel de [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) a déjà été ajouté dans la requête de performances. Ce compteur est ignoré.
| 0xC0000BF7 ( \_ \_ fichier journal binaire PDH \_ endommagé)                       | Impossible de lire les informations de compteur et les données des fichiers journaux binaires d’entrée.
| 0xC0000BF8 ( \_ exemple de journal PDH \_ \_ trop \_ petit)                    | Au moins l’un des fichiers journaux binaires d’entrée contient moins de deux échantillons de données.
| 0xC0000BF9 ( \_ version ultérieure du système d’exploitation PDH \_ \_ )                         | La version du système d’exploitation sur l’ordinateur nommé %1 est ultérieure à celle de l’ordinateur local. Cette opération n’est pas disponible à partir de l’ordinateur local.
| 0xC0000BFA ( \_ version antérieure du système d’exploitation PDH \_ \_ )                       | %1 prend en charge %2 ou une version ultérieure. Vérifiez la version du système d’exploitation sur l’ordinateur nommé %3.
| 0xC0000BFB ( \_ heure d’ajout incorrecte PDH \_ \_ )                    | Le fichier de sortie doit contenir des données antérieures à celles du fichier à ajouter.
| 0xC0000BFC ( \_ compteur d’ajout non APpariés PDH \_ \_ )                 | Les deux fichiers doivent avoir des compteurs identiques pour pouvoir être ajoutés.
| 0xC0000BFD (PDH \_ SQL \_ ALTER \_ DETAIL \_ failed)                 | impossible de modifier la disposition de la table CounterDetail dans SQL base de données.
| 0xC0000BFE ( \_ requête PDH \_ \_ délai d’expiration des données de performance \_ )                 | Le système est occupé. Un délai d’attente A été dépassé lors de la collecte des données de compteur. Réessayez plus tard ou augmentez la valeur de Registre **CollectTime** .
