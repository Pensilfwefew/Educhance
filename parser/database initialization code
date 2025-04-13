--
-- PostgreSQL database dump
--

-- Dumped from database version 16.8
-- Dumped by pg_dump version 16.8

-- Started on 2025-04-13 17:40:09

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

SET default_tablespace = '';

SET default_table_access_method = heap;

--
-- TOC entry 222 (class 1259 OID 16751)
-- Name: ball; Type: TABLE; Schema: public; Owner: postgres
--

CREATE TABLE public.ball (
    id_ball integer NOT NULL,
    ball text,
    year integer,
    id_directions integer
);


ALTER TABLE public.ball OWNER TO postgres;

--
-- TOC entry 221 (class 1259 OID 16750)
-- Name: ball_id_ball_seq; Type: SEQUENCE; Schema: public; Owner: postgres
--

CREATE SEQUENCE public.ball_id_ball_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER SEQUENCE public.ball_id_ball_seq OWNER TO postgres;

--
-- TOC entry 4885 (class 0 OID 0)
-- Dependencies: 221
-- Name: ball_id_ball_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: postgres
--

ALTER SEQUENCE public.ball_id_ball_seq OWNED BY public.ball.id_ball;


--
-- TOC entry 220 (class 1259 OID 16737)
-- Name: directions; Type: TABLE; Schema: public; Owner: postgres
--

CREATE TABLE public.directions (
    id_directions integer NOT NULL,
    id_institutes integer,
    fac text,
    direction text,
    level_program text,
    code_program text,
    profile_program text,
    form_study text
);


ALTER TABLE public.directions OWNER TO postgres;

--
-- TOC entry 219 (class 1259 OID 16736)
-- Name: directions_id_directions_seq; Type: SEQUENCE; Schema: public; Owner: postgres
--

CREATE SEQUENCE public.directions_id_directions_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER SEQUENCE public.directions_id_directions_seq OWNER TO postgres;

--
-- TOC entry 4886 (class 0 OID 0)
-- Dependencies: 219
-- Name: directions_id_directions_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: postgres
--

ALTER SEQUENCE public.directions_id_directions_seq OWNED BY public.directions.id_directions;


--
-- TOC entry 224 (class 1259 OID 16808)
-- Name: exam; Type: TABLE; Schema: public; Owner: postgres
--

CREATE TABLE public.exam (
    id_exam integer NOT NULL,
    id_directions integer,
    exam text,
    view text
);


ALTER TABLE public.exam OWNER TO postgres;

--
-- TOC entry 223 (class 1259 OID 16807)
-- Name: exam_id_exam_seq; Type: SEQUENCE; Schema: public; Owner: postgres
--

CREATE SEQUENCE public.exam_id_exam_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER SEQUENCE public.exam_id_exam_seq OWNER TO postgres;

--
-- TOC entry 4887 (class 0 OID 0)
-- Dependencies: 223
-- Name: exam_id_exam_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: postgres
--

ALTER SEQUENCE public.exam_id_exam_seq OWNED BY public.exam.id_exam;


--
-- TOC entry 216 (class 1259 OID 16714)
-- Name: gorod; Type: TABLE; Schema: public; Owner: postgres
--

CREATE TABLE public.gorod (
    id_gorod integer NOT NULL,
    href text,
    city text
);


ALTER TABLE public.gorod OWNER TO postgres;

--
-- TOC entry 215 (class 1259 OID 16713)
-- Name: gorod_id_gorod_seq; Type: SEQUENCE; Schema: public; Owner: postgres
--

CREATE SEQUENCE public.gorod_id_gorod_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER SEQUENCE public.gorod_id_gorod_seq OWNER TO postgres;

--
-- TOC entry 4888 (class 0 OID 0)
-- Dependencies: 215
-- Name: gorod_id_gorod_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: postgres
--

ALTER SEQUENCE public.gorod_id_gorod_seq OWNED BY public.gorod.id_gorod;


--
-- TOC entry 218 (class 1259 OID 16723)
-- Name: institutes; Type: TABLE; Schema: public; Owner: postgres
--

CREATE TABLE public.institutes (
    id_institutes integer NOT NULL,
    id_gorod integer,
    full_name text,
    name_small text,
    href text
);


ALTER TABLE public.institutes OWNER TO postgres;

--
-- TOC entry 217 (class 1259 OID 16722)
-- Name: institutes_id_institutes_seq; Type: SEQUENCE; Schema: public; Owner: postgres
--

CREATE SEQUENCE public.institutes_id_institutes_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER SEQUENCE public.institutes_id_institutes_seq OWNER TO postgres;

--
-- TOC entry 4889 (class 0 OID 0)
-- Dependencies: 217
-- Name: institutes_id_institutes_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: postgres
--

ALTER SEQUENCE public.institutes_id_institutes_seq OWNED BY public.institutes.id_institutes;


--
-- TOC entry 4711 (class 2604 OID 16754)
-- Name: ball id_ball; Type: DEFAULT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.ball ALTER COLUMN id_ball SET DEFAULT nextval('public.ball_id_ball_seq'::regclass);


--
-- TOC entry 4710 (class 2604 OID 16740)
-- Name: directions id_directions; Type: DEFAULT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.directions ALTER COLUMN id_directions SET DEFAULT nextval('public.directions_id_directions_seq'::regclass);


--
-- TOC entry 4712 (class 2604 OID 16811)
-- Name: exam id_exam; Type: DEFAULT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.exam ALTER COLUMN id_exam SET DEFAULT nextval('public.exam_id_exam_seq'::regclass);


--
-- TOC entry 4708 (class 2604 OID 16717)
-- Name: gorod id_gorod; Type: DEFAULT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.gorod ALTER COLUMN id_gorod SET DEFAULT nextval('public.gorod_id_gorod_seq'::regclass);


--
-- TOC entry 4709 (class 2604 OID 16726)
-- Name: institutes id_institutes; Type: DEFAULT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.institutes ALTER COLUMN id_institutes SET DEFAULT nextval('public.institutes_id_institutes_seq'::regclass);


--
-- TOC entry 4877 (class 0 OID 16751)
-- Dependencies: 222
-- Data for Name: ball; Type: TABLE DATA; Schema: public; Owner: postgres
--